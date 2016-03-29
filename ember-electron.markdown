# Building Ember Apps with Electron
## How Electron works
- Main process spins up renderer subprocesses

## Ember-Electron
- Build/Run with live reload
- Ember inspector
- Build packaging for install files
- `ember install ember-electron`
- Executes `electron.js`
- Doesn't run a server
- To run `ember electron`
- Can inspect with Chrome inspector
- `ember electron:test` to test

## Short comings
- No context menu by default
- No copy and paste
- No spellcheck API
- Native builds require native build tools
- Cross site scripting attacks can access lots more stuff through native APIs

## Benefits of Native Code
- SQL performance benefits
- Keytar for storing API keys
