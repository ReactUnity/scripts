# React Unity Scripts

This package includes scripts and configuration used by [React Unity](https://github.com/ReactUnity/core).<br>
Please refer to its documentation:

- [Getting Started](https://facebook.github.io/create-react-app/docs/getting-started) – How to create a new app.
- [User Guide](https://facebook.github.io/create-react-app/) – How to develop apps bootstrapped with Create React App.

## Extra Environment Variables

- `FILENAME` - Name of the generated javascript file. `index.js` by default.
- `BUILD_DIR` - Path to the generated output. Relative to the project. `build` by default.
- `GENERATE_SOURCEMAP` - `false` by default.
- `HARD_RELOAD` - Reload the entire UI instead of doing HMR. `false` by default.
- `IMAGE_INLINE_SIZE_LIMIT` - `0` by default. Because non-inlined images will be faster in Unity. However, users may still want to inline images.

Environment variables can also be defined by having `.env`, `.env.local`, `.env.<development|production>` in project folder.
