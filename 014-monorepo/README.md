# ESLint on monorepos

by default eslint will search from the current directory to up the root, and will merge all the rules in one file. 

To stop this behavior only set `root: true` in the eslintrc file.