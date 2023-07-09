# Hexagonal Architecture with ESLint 💥

add the plugin: [Codely](https://www.npmjs.com/package/eslint-plugin-hexagonal-architecture)
```json
plugins: ["hexagonal-architecture"],
overrides: [
	{
    files: ["src/**/*.ts"],
    rules: {
      "hexagonal-architecture/enforce": ["error"],
    },
  },
]
```