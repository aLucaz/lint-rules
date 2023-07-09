# Configuration Details 👀
- ESlint uses javascript ES5 by default
- it can be extended to use Typescript and other ES version

## Lets go from the beginning
1. Add simple rules to your eslintrc file
```json
"rules": {
    "semi": ["error", "always"],
    "quotes": ["error", "double"],
    "@typescript-eslint/no-non-null-assertion": "off"
  },
```
*This config only include the JS files.*
2. To use the typescript parser add:
```json
"parser": "@typescript-eslint/parser",
```
3. To add more rules as block add:
```json
"extends": [
  "eslint:recommended", 
  "plugin:@typescript-eslint/recommended"
],
"plugins": ["@typescript-eslint"],
```
*This config includes general rules to avoid bugs.*
*The plugin is used to add all the rules and the extends is to get recommended ones*
4. To tell ESLint the environment where the project is running add:
```json
  env: {
    node: true,
    jest: true,
  },
```
5. To override or deactivate specific rules add:
```json
  overrides: [
    {
      files: ["*.js"],
      rules: {
        "@typescript-eslint/no-unsafe-assignment": "off",
        "@typescript-eslint/no-unsafe-call": "off",
        "@typescript-eslint/no-unsafe-member-access": "off",
        "@typescript-eslint/no-var-requires": "off",
      },
    },
  ],
```