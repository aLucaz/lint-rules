# editorconfig
formatting rules based on dotfiles
it supports multiple languages, not only js and ts

# advantages
is directly supported by github editor and previsualizer, so you can configure it to avoid some unnecesary rules.

you can use it by downloading a plugin and creating a file .editorconfig with the rules.

# editorconfig and ESlint? 👀
you can use both using the plugin:
```json
extends: [
  "eslint:recommended",
  "plugin:@typescript-eslint/recommended",
  "plugin:editorconfig/all",
  "plugin:editorconfig/noconflict",
],
plugins: ["editorconfig"],
```
