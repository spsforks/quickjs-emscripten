# @jitl/quickjs-node-release-sync-wasm

Node.js build with both CommonJS and ESModule exports

This generated package is part of [quickjs-emscripten](https://github.com/justjake/quickjs-emscripten).
It contains a variant of the quickjs WASM library, and can be used with quickjs-emscripten-core.

```typescript
import variant from "@jitl/quickjs-node-release-sync-wasm"
import { newQuickJSWASMModuleFromVariant } from "quickjs-emscripten-core"
const QuickJS = await newQuickJSWASMModuleFromVariant(variant)
```

This variant was built with the following settings:

## Library: quickjs

The original [bellard/quickjs](https://github.com/bellard/quickjs) library.

## Release mode: release

Optimized for performance; use when building/deploying your application.

## Module system: both

Contains both CommonJS and ESModule exports.

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
  "description": "Node.js build with both CommonJS and ESModule exports",
  "emscriptenEnvironment": ["node"],
  "moduleSystem": "both"
}
```

Variant-specific Emscripten build flags:

```json
["-Oz", "-flto", "--closure 1", "-s FILESYSTEM=0", "-s ENVIRONMENT=node"]
```