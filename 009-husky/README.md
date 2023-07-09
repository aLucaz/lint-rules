# Husky 🐻

Rules to improve team workflow by executing githooks in a simple way.

You can see the intall process [here](https://www.npmjs.com/package/husky).

# Details

You can run the linter --fix using the package: lint-staged
```json
  "devDependencies": {
    "husky": "^8.0.1",
    "lint-staged": "^13.0.3",
  },
  "lint-staged": {
    "*.(j|t)s": "eslint --fix"
  }
```
this will add the lint --fix changes to the commit
to run it the pre-commit file will contain:
`npx lint-staged`

# Recommendations
- pre-commit
  - run here fast things like the linter & formaters
- pre-push
  - run here maybe some tests

# Tricks

you can avoid using husky by doing:
`git commit -m "test" --no-verify`

to avoid this you can add the npm run lint on the ci pipelines