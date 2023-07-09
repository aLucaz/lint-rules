# plugins
to add plugins you can add:
*All the plugins need to be added on the package.json also*
```json
"plugins": [
  "@typescript-eslint", 
  "simple-import-sort", 
  "import", 
  "unused-imports", 
  "folders"
],
```
*this is not enough cause you need to add the rules to apply the plugins*

rules:

```json
  "rules": {
    "semi": ["error", "always"],
    "quotes": ["error", "double"],
    "import/first": "error",
    "import/newline-after-import": "error",
    "import/no-duplicates": "error",
    "import/no-webpack-loader-syntax": "error",
    "folders/match-regex": ["error", "^[a-z-]+$", "/js/"],
    "simple-import-sort/exports": "error",
    "simple-import-sort/imports": "error",
    "unused-imports/no-unused-imports": "error",
    "unused-imports/no-unused-vars": [
      "warn",
      {
        vars: "all",
        varsIgnorePattern: "^_",
        args: "after-used",
        argsIgnorePattern: "^_",
      },
    ],
    "@typescript-eslint/no-non-null-assertion": "off"
  },
```

also you can configure the order of imports:

```json
"simple-import-sort/imports": [
  "error",
  {
    groups: [
      // Imports que producen side effects: `import "./setup";`
      ["^\\u0000"],
      // Paquetes: `import fs from "fs";`
      ["^@?\\w"],
      // Paquetes internos.
      ["^(@|@codely)(/.*|$)"],
      // Imports de niveles superiores.
      ["^\\.\\.(?!/?$)", "^\\.\\./?$"],
      // Otros imports relativos. De la misma carpeta y `.` al final.
      ["^\\./(?=.*/)(?!/?$)", "^\\.(?!/?$)", "^\\./?$"],
      // Imports de estilo.
      ["^.+\\.s?css$"],
    ],
  },
],
```