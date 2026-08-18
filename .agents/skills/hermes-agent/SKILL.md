```markdown
# hermes-agent Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `hermes-agent` TypeScript repository. It covers file naming, import/export styles, commit message conventions, and testing patterns. By following these guidelines, contributors can maintain consistency and quality across the codebase.

## Coding Conventions

### File Naming
- **Style:** kebab-case
- **Example:**  
  ```
  hermes-agent.ts
  message-handler.test.ts
  ```

### Import Style
- **Style:** Relative imports  
- **Example:**
  ```typescript
  import { sendMessage } from './message-utils';
  ```

### Export Style
- **Style:** Named exports  
- **Example:**
  ```typescript
  export function sendMessage() { ... }
  export const AGENT_VERSION = '1.0.0';
  ```

### Commit Messages
- **Style:** Conventional commits
- **Prefix:** `chore`
- **Average length:** ~77 characters
- **Example:**
  ```
  chore: update dependencies to latest versions for security patches
  ```

## Workflows

### Code Contribution
**Trigger:** When adding new features, fixing bugs, or making changes  
**Command:** `/contribute`

1. Create a new branch using kebab-case for the branch name.
2. Write code using relative imports and named exports.
3. Name all new files in kebab-case.
4. Write or update tests in files matching `*.test.*`.
5. Commit changes using the conventional commit style (e.g., `chore: ...`).
6. Open a pull request for review.

### Dependency Update
**Trigger:** When dependencies need to be updated  
**Command:** `/update-dependencies`

1. Pull the latest changes from the main branch.
2. Update dependencies as needed.
3. Test the application to ensure compatibility.
4. Commit using `chore: update dependencies ...`.
5. Push and open a pull request.

## Testing Patterns

- **Test File Naming:**  
  Test files follow the pattern `*.test.*` (e.g., `message-handler.test.ts`).
- **Framework:**  
  No specific testing framework detected; follow repository conventions or consult maintainers.
- **Example Test File:**
  ```typescript
  import { sendMessage } from './message-utils';

  describe('sendMessage', () => {
    it('should send a message successfully', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command                | Purpose                                      |
|------------------------|----------------------------------------------|
| /contribute            | Step-by-step guide for contributing code     |
| /update-dependencies   | Instructions for updating dependencies       |
```
