[quickjs-emscripten](../../packages.md) • **@jitl/quickjs-node-cjs-release-sync-wasm** • [Readme](README.md) \| [Exports](exports.md)

***

# @jitl/quickjs-node-cjs-release-sync-wasm

Node.js CommonJS module

This generated package is part of [quickjs-emscripten](https://github.com/justjake/quickjs-emscripten).
It contains a variant of the quickjs WASM library, and can be used with quickjs-emscripten-core.

```typescript
import variant from "@jitl/quickjs-node-cjs-release-sync-wasm"
import { newQuickJSWASMModuleFromVariant } from "quickjs-emscripten-core"
const QuickJS = await newQuickJSWASMModuleFromVariant(variant)
```

This variant was built with the following settings:

## Contents

- [Library: quickjs](README.md#library-quickjs)
- [Release mode: release](README.md#release-mode-release)
- [Module system: commonjs](README.md#module-system-commonjs)
- [Extra async magic? No](README.md#extra-async-magic-no)
- [Single-file, or separate .wasm file? wasm](README.md#single-file-or-separate-wasm-file-wasm)
- [More details](README.md#more-details)

## Library: quickjs

The original [bellard/quickjs](https://github.com/bellard/quickjs) library.

## Release mode: release

Optimized for performance; use when building/deploying your application.

## Module system: commonjs

This variant exports a CommonJS module, which is faster to load and run in Node.js.

## Extra async magic? No

The default, normal build. Note that both variants support regular async functions.

## Single-file, or separate .wasm file? wasm

Has a separate .wasm file. May offer better caching in your browser, and reduces the size of your JS bundle. If you have issues, try a 'singlefile' variant.

## More details

Full variant JSON description:

```json
{
  "library": "quickjs",
  "releaseMode": "release",
  "syncMode": "sync",
  "emscriptenInclusion": "wasm",
  "description": "Node.js CommonJS module",
  "emscriptenEnvironment": ["node"],
  "moduleSystem": "commonjs"
}
```

Variant-specific Emscripten build flags:

```json
["-Oz", "-flto", "-s SINGLE_FILE=1", "--closure 1", "-s FILESYSTEM=0", "-s ENVIRONMENT=node"]
```

***

Generated using [typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown) and [TypeDoc](https://typedoc.org/)