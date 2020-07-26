# Extensions

Extensions are mods that run some JavaScript
## Fields

```typescript
export interface Extension extends Metadata {
  entry?: string | string[]
  loadBeforeGame?: boolean
  applyServer?: number[]
  resourcepack?: Array<string | ResourcePackReplaceEntry>
}
```

| Field           | Type                                       | Default value      | Description                                                     |
| -------------- | ------------------------------------------ | ----------- | -------------------------------------------------------- |
| entry          | `string | string[]`                        | `script.js` | Run the js code.                                 |
| loadBeforeGame | `boolean`                                  | `false`     | Run before the game                           |
| applyServer    | `number[]`                                 | `[0, 1, 2]` | Which server is to be run. 0 China，1 Japan，2 EN |
| resourcepack   | `Array<string ResourcePackReplaceEntry>` | `[]`        | Replaces files like a resourcepack      |

## Node compatible？
?
