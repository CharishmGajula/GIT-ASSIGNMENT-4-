# GIT-ASSIGNMENT-4

# HOOKS
Hooks are the script files present in .git/hooks

These helps us for the atomation.

Like if are about to make a commit, we should know if everything is correct or not, is formatting correct or not, Hooks come to play at this point, Helps in just stopping the commit and checking the code changes. If error is present then commit will not happen.

Commonly Used commits are:

  pre-commit: Runs before a commit is finalized.
  
  commit-msg: Validates the commit message.
  
  pre-push: Runs before pushing code to a remote repository.
  
  ![image](https://github.com/user-attachments/assets/93d265f6-d41f-4aaa-b6a3-2a46b097c278)
  
In this way Hooks helps us from not doing bad in the code.



# HUSKY
Husky is a tool Which makes it easy for Hooks.

Instead of writing all the script for hooks we can just Configue the commands of husky.

Husky run tasks such as linting, formatting, or tests before code is committed, helping enforce code quality and prevent bad code from entering your repository.

# When ever you give a command git commit
then husky will

Trigger the pre-commit hook.

Run lint-staged.

Lint and format the staged .js files.

Block the commit if errors are found.

Install Husky --> npm install husky

Rules can be written like
{
  "rules": {
    "no-unused-vars": "error",
    "semi": ["error", "always"]
  }
}

# Tasks we Can do with Husky
Lint staged files --> Formatting --> pre-commit

Run tests before push --> Run tests before push --> pre-push

Enforce commit message style --> Validating commit messages --> commit-msg

Prevent debug code commits --> Block console.log or TODOs --> pre-commit

Type check code--> Ensure type safety with TypeScript --> pre-commit
