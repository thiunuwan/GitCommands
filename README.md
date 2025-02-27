## Useful Git Commands

### Update .gitignore

When you update your `.gitignore` file, you might need to remove previously tracked files that are now supposed to be ignored. Here are the steps to achieve this:

1. **Remove all files from the staging area (but keep them in the working directory):**
    ```sh
    git rm -r --cached .
    ```
    This command untracks all files currently being tracked by Git, without deleting them from your local directory.

2. **Re-add all files, applying the .gitignore rules:**
    ```sh
    git add .
    ```
    This command stages all files, but this time it respects the .gitignore file, so ignored files won’t be added.

3. **Commit the changes:**
    ```sh
    git commit -m "Update .gitignore"
    ```
    This command commits the changes to your local repository with a message explaining what you did.
