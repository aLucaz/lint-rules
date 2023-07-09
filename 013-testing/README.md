# ESLint on tests
eslint also can be applied on jest using this plugins:
- [eslint-plugin-jest](https://www.npmjs.com/package/eslint-plugin-jest) general
- [eslint-plugin-jest-dom](https://github.com/testing-library/eslint-plugin-jest-dom) for frontend dom specific testing
- [eslint-plugin-testing-library](https://github.com/testing-library/eslint-plugin-testing-library) for frontend testing

override to only apply the plugin on test files:
```json
  overrides: [
    {
      files: ["tests/*.spec.js"],
      extends: [
        "plugin:jest/recommended",
        "plugin:jest/style",
        "plugin:jest-dom/recommended",
        "plugin:testing-library/dom",
      ],
    },
  ],
```