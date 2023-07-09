# Prettier 🔥

is a formatter that has some rules that are configurables but all the new rules that they add are not changable.

is not only for js and ts, also have rules for html, css, markdown, yaml, json, etc.

# how to work with ESLint

```json
extends: [
    "plugin:prettier/recommended",
  ],
```
this will deactivate the eslint rules that can have conflicts with prettier.
*This must be added to work with eslint*

hey 👀
There is other plugin: eslint-plugin-prettier, that transform prettier rules into eslint rules, this is used to run everything on eslint. Without this prettier runs as a separated process.

This will mark the style notifications as errors also!

to add that you have to install: 

```json
    "eslint-config-prettier": "^8.5.0",
    "eslint-plugin-prettier": "^4.2.1",
```
and the plugin line on the `extends` section in the eslintrc file.

# find conflicts

to see if there are rules that can cause problems:

`npx eslint-config-prettier ./*.*`
