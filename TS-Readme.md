# strict vs alwaysStrict

It is a good idea to not only include `alwaysStrict`, but to include the strict flag that enables alwaysStrict and also `noImplicitAny`, `noImplicitThis`, `strictBindCallApply`, `strictNullChecks`, `strictFunctionTypes`, `strictPropertyInitialization` and `useUnknownInCatchVariables` which are even more important.

The `alwaysStrict` TypeScript flag parses your files in parses in the JS strict mode (as opposed to the JS sloppy mode and emits `'use strict'` in the output. Instead of using the alwaysStrict flag you could add "`use strict`"; to all of your files (the ES modules are strict by default).

# Is source map safe?

A source map is obviously helpful for debugging, but it also raises security concerns. It can expose a program's or website's original source code, which may reveal things like passwords or private data.

# If the typeRoots property is not defined in the tsconfig.json file?

The TypeScript compiler will default to including all folders under the `node_modules/@type`s directory by default. This means that any installed TypeScript declaration files in the @types folder of the node_modules directory will be automatically included and considered part of the project's type definition.

# If the types property is not defined in the tsconfig.json file?

TypeScript will automatically include all TypeScript declaration files (.d.ts) located in the `typeRoots` directories, as well as the `node_modules/@types` directory.

# importHelpers

Enabling the importHelpers option in TypeScript can provide benefits in terms of reducing code duplication and optimizing bundle sizes, especially when using features like async/await or dynamic import (import()) extensively in your codebase

When importHelpers is enabled, TypeScript emits helper functions like **awaiter and **generator to the tslib module, reducing code duplication and bundle size. Ensure tslib is available by including it as a dependency or configuring your bundler.

# jsx

The "jsx": "preserve" option in the tsconfig.json file specifies how TypeScript should handle JSX (JavaScript XML) syntax during the compilation process.

When "jsx" is set to "preserve", TypeScript will keep the JSX syntax intact in the generated JavaScript output. It will not transpile JSX syntax into regular function calls or React-specific code. This is useful when you are using a separate tool or build process (like Babel) to handle JSX transformation.
