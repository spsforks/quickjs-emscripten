[quickjs-emscripten](../../packages.md) • **@jitl/quickjs-browser-debug-asyncify-singlefile** • [Readme](README.md) \| [Exports](exports.md)

***

[quickjs-emscripten](../../packages.md) / @jitl/quickjs-browser-debug-asyncify-singlefile

# @jitl/quickjs-browser-debug-asyncify-singlefile

## Contents

- [Variables](exports.md#variables)
  - [default](exports.md#default)
  - [[@jitl/quickjs-browser-debug-asyncify-singlefile](https://github.com/justjake/quickjs-emscripten/blob/main/doc/packages/@jitl/quickjs-browser-debug-asyncify-singlefile/README.md)](exports.md#jitlquickjs-browser-debug-asyncify-singlefilehttpsgithubcomjustjakequickjs-emscriptenblobmaindocpackagesjitlquickjs-browser-debug-asyncify-singlefilereadmemd)

## Variables

### default

> **`const`** **default**: `Object`

This export is a variant of the quickjs WASM library:
### [@jitl/quickjs-browser-debug-asyncify-singlefile](https://github.com/justjake/quickjs-emscripten/blob/main/doc/packages/@jitl/quickjs-browser-debug-asyncify-singlefile/README.md)

ESModule for browsers or browser-like environments

| Variable            |    Setting                     |    Description    |
| --                  | --                             | --                |
| releaseMode         | debug | Enables assertions and memory sanitizers. Try to run your tests against debug variants, in addition to your preferred production variant, to catch more bugs. |
| syncMode            | asyncify | Build run through the ASYNCIFY WebAssembly transform. Larger and slower. Allows synchronous calls from the WASM runtime to async functions on the host. The extra magic makes this variant slower than sync variants. Note that both variants support regular async functions. Only adopt ASYNCIFY if you need to! |
| moduleSystem        | esm | This variant exports an ESModule, which is standardized for browsers and more modern browser-like environments. It cannot be imported from CommonJS without shenanigans. |
| emscriptenInclusion | singlefile | The WASM runtime is included directly in the JS file. Use if you run into issues with missing .wasm files when building or deploying your app. |

#### Type declaration

##### importFFI

> **`readonly`** **importFFI**: () => `Promise`\<*typeof* `QuickJSAsyncFFI` \| (`module`) => [`QuickJSAsyncFFI`](../../quickjs-emscripten/interfaces/QuickJSAsyncFFI.md)\>

###### Returns

`Promise`\<*typeof* `QuickJSAsyncFFI` \| (`module`) => [`QuickJSAsyncFFI`](../../quickjs-emscripten/interfaces/QuickJSAsyncFFI.md)\>

##### importModuleLoader

> **`readonly`** **importModuleLoader**: () => `Promise`\<[`EmscriptenModuleLoader`](../../quickjs-emscripten/interfaces/EmscriptenModuleLoader.md)\<[`QuickJSAsyncEmscriptenModule`](../../quickjs-emscripten/interfaces/QuickJSAsyncEmscriptenModule.md)\> \| `Object` \| `Object`\>

###### Returns

`Promise`\<[`EmscriptenModuleLoader`](../../quickjs-emscripten/interfaces/EmscriptenModuleLoader.md)\<[`QuickJSAsyncEmscriptenModule`](../../quickjs-emscripten/interfaces/QuickJSAsyncEmscriptenModule.md)\> \| `Object` \| `Object`\>

##### type

> **`readonly`** **type**: `"async"` = `"async"`

#### Source

[variant-quickjs-browser-debug-asyncify-singlefile/dist/index.ts:17](https://github.com/justjake/quickjs-emscripten/blob/main/packages/variant-quickjs-browser-debug-asyncify-singlefile/dist/index.ts#L17)

***

Generated using [typedoc-plugin-markdown](https://www.npmjs.com/package/typedoc-plugin-markdown) and [TypeDoc](https://typedoc.org/)