# Rules tunning

- no-restricted-imports: avoid importing files from determined pattern
```json
    "no-restricted-imports": [
      "warn", 
      {
        patterns: [{ 
          group: ["**/utils"],
          message: "Please use or move the utils method to shared folder."
        }]
      }, 
    ],
```