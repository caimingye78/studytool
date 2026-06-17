```markdown
# studytool Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `studytool` JavaScript repository. You'll learn how to structure files, write imports/exports, follow commit message conventions, and write and run tests. These guidelines ensure consistency and maintainability across the codebase.

## Coding Conventions

### File Naming
- Use **snake_case** for all filenames.
  - Example: `user_profile.js`, `data_manager.test.js`

### Import Style
- Use **relative imports** for modules.
  - Example:
    ```javascript
    import { fetchData } from './data_manager.js';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```javascript
    // In data_manager.js
    export function fetchData() { ... }
    ```

### Commit Messages
- Follow the **conventional commit** format.
- Prefixes used: `feat`, `docs`
- Example:
  ```
  feat: add user authentication module
  docs: update README with setup instructions
  ```

## Workflows

### Creating a New Feature
**Trigger:** When adding new functionality
**Command:** `/new-feature`

1. Create a new file using snake_case (e.g., `feature_name.js`).
2. Write your code, using named exports.
3. Import any dependencies using relative paths.
4. Write a corresponding test file (`feature_name.test.js`).
5. Commit your changes using a `feat:` prefix.
   ```
   feat: implement [feature description]
   ```

### Writing Documentation
**Trigger:** When updating or adding documentation
**Command:** `/write-docs`

1. Edit or create documentation files as needed.
2. Use clear, concise language.
3. Commit your changes using a `docs:` prefix.
   ```
   docs: add usage examples to README
   ```

### Running Tests
**Trigger:** Before pushing or merging changes
**Command:** `/run-tests`

1. Identify all files matching the `*.test.*` pattern.
2. Run your preferred test runner (framework not specified).
3. Ensure all tests pass before committing.

## Testing Patterns

- Test files follow the `*.test.*` naming convention (e.g., `data_manager.test.js`).
- The specific test framework is not specified; use your team's standard.
- Example test file structure:
  ```javascript
  import { fetchData } from './data_manager.js';

  test('fetchData returns correct data', () => {
    // test implementation
  });
  ```

## Commands

| Command        | Purpose                                 |
|----------------|-----------------------------------------|
| /new-feature   | Scaffold and commit a new feature       |
| /write-docs    | Add or update documentation             |
| /run-tests     | Run all test files before committing    |
```
