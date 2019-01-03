# Node

`tsconfig.json`
```
{
    "compilerOptions": {
        "outDir": "./dist/",
        "module": "commonjs",
        "lib": [
            "esnext",
            "dom"
        ],
        "target": "esnext",
        "sourceMap": true,
        "allowSyntheticDefaultImports": true,
        "strict": true,
        "allowJs": true
    },
    "include": [
        "src/**/*"
    ],
    "exclude": [
        "node_modules",
        "dist"
    ]
}
```

`--inspect-brk` will add a breakpoint to the first line, waiting for a debugger to attach before continuing
`--inspect` will allow you to attach a debugger as the process is running

Use `node --inspect -r ts-node` to run the source
Or `tsc && node --inspect dist/index`

Use the following in VSCode `launch.json` to skip annoying internal node debug
```
"smartStep": true,
"skipFiles": ["<node_internals>/**"],
```
