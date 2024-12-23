# Tauri v2

Rust backend (need to work with Rust environment)


## Installation

Requires Rust and NodeJs


Install Tauri cli


## Dev

```bash
pnpm taur dev
```

## Vanilla JS

### Folders

```/src```        Source files for HTML/JS/CSS

```/src-tauri```  Source files for Rust


Set: ```"withGlobalTauri": true,```

```javascript
const { invoke } = window.__TAURI__.core;
const { event, window: tauriWindow, path } = window.__TAURI__;
```

## Building

Executables location: ```src-tauri\target\release```


