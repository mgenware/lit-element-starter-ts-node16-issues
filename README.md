To demonstrate compile issues of [lit-element-starter-ts](https://github.com/lit/lit-element-starter-ts) and TypeScript 4.7 Node16 module.

This is a fork of [lit-element-starter-ts](https://github.com/lit/lit-element-starter-ts) with the following changes:

- Upgraded dependencies
- Update `tsconfig.json` to use TypeScript 4.7 `node16`:
  - Set `module` to `node16`
  - Set `moduleResolution` to `node16`

To repro the issue:

- Clone this repo
- Install dependencies `npm i`
- Run `npm run build && npm test`.

Output:

```
node_modules/@open-wc/semantic-dom-diff/chai-dom-diff-plugin.d.ts:3:29 - error TS2835: Relative import paths need explicit file extensions in EcmaScript imports when '--moduleResolution' is 'node16' or 'nodenext'. Did you mean './get-diffable-html.js'?

3 import { DiffOptions } from "./get-diffable-html";
                              ~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:3:22 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

3 export { html } from '@open-wc/testing-helpers';
                       ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:4:30 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

4 export { unsafeStatic } from '@open-wc/testing-helpers';
                               ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:5:32 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

5 export { triggerBlurFor } from '@open-wc/testing-helpers';
                                 ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:6:33 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

6 export { triggerFocusFor } from '@open-wc/testing-helpers';
                                  ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:7:26 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

7 export { oneEvent } from '@open-wc/testing-helpers';
                           ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:8:22 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

8 export { isIE } from '@open-wc/testing-helpers';
                       ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:9:26 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

9 export { defineCE } from '@open-wc/testing-helpers';
                           ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:10:26 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

10 export { aTimeout } from '@open-wc/testing-helpers';
                            ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:11:27 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

11 export { nextFrame } from '@open-wc/testing-helpers';
                             ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:12:28 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

12 export { litFixture } from '@open-wc/testing-helpers';
                              ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:13:32 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

13 export { litFixtureSync } from '@open-wc/testing-helpers';
                                  ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:14:25 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

14 export { fixture } from '@open-wc/testing-helpers';
                           ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:15:29 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

15 export { fixtureSync } from '@open-wc/testing-helpers';
                               ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:16:32 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

16 export { fixtureCleanup } from '@open-wc/testing-helpers';
                                  ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:17:32 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

17 export { elementUpdated } from '@open-wc/testing-helpers';
                                  ~~~~~~~~~~~~~~~~~~~~~~~~~~

node_modules/@open-wc/testing/index.d.ts:18:27 - error TS7016: Could not find a declaration file for module '@open-wc/testing-helpers'. '/Users/m/lit-element-starter-ts/node_modules/@open-wc/testing-helpers/index.js' implicitly has an 'any' type.
  Try `npm i --save-dev @types/open-wc__testing-helpers` if it exists or add a new declaration (.d.ts) file containing `declare module '@open-wc/testing-helpers';`

18 export { waitUntil } from '@open-wc/testing-helpers';
                             ~~~~~~~~~~~~~~~~~~~~~~~~~~


Found 17 errors in 2 files.
```
