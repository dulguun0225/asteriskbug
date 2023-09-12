# Nested/transitive dependency * asterisk version bug

### The `@types/react-transition-group` package has a dependency as
```json
"@types/react" : "*"
```
### This project has a dependency as
```json
"@types/react": "^16.9.56"
```
Also both overrides and resolutions as
```json
  "overrides": {
    "@types/react": "^16.9.56"
  },
  "resolutions": {
    "@types/react": "^16.9.56"
  },
```

### After running 
```bash
bun install
```

The `node_modules/react-transition-group/node_modules/@types/react` should not exist

