# babel-eslint flow import issue

1. `npm ci`
2. `npm test`

Result:

```
/home/lydell/stuff/babel-eslint/test.js
  4:3  error  Parsing error: Imports within a `declare module` body must always be `import type` or `import typeof`

  2 | 
  3 | declare module "cross-spawn" {
> 4 |   import typeof childProcess from "child_process";
    |   ^
  5 | 
  6 |   declare module.exports: {
  7 |     sync: $PropertyType<childProcess, "spawnSync">,

✖ 1 problem (1 error, 0 warnings)
```

Expected: No output.
