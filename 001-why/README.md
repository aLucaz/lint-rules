# Advantages 🚀
- can help the team to maintain a clear and common style of code
- detect bugs on development time
- avoid merge conflicts
- easy to use 
- prevent errors

# Where can be used
- inconsistent spacing on imports
- unordered imports
- bad use of let and const
- trailing comma
- bad code styling
- many many more 

# Tricks
- when eslint is not being applied you can run: "Restart ESlint server" to restart the project
- when you want to apply ESlint on a legacy project you can run `npx eslint-nibble ./src/*ts` and it will list the quantity of erros by rule, then you can apply changes based on it.
- when you have a monorepo with isolated projects, sometimes you need to configure the .vscode to apply all the rules:
```json
{
  "eslint.workingDirectories": [
    "./1-1-why-linting",
    "./1-2-basic-config",
    "./2-1-rules",
    "./2-2-plugins",
    "./2-3-editorconfig",
    "./3-1-bug-prevention",
    "./3-2-good-practises",
    "./3-3-architecture",
  ]
}
```
- 

# Basic configuration
