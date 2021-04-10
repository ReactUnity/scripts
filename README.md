# React Unity Scripts

![npm version](https://badge.fury.io/js/%40reactunity%2Fscripts.svg)

This package includes scripts and configuration used by [React Unity](https://github.com/ReactUnity/core).

This project is a fork of [Create React App (CRA)](https://create-react-app.dev/). Same options, conventions, and environment variables can be used. You can also check the documentation of CRA to get more information.

## Installation

```
npm i @reactunity/scripts
```

## Commands

- `react-unity-scripts start` - Start the dev server with Hot Module Replacement (HMR)
- `react-unity-scripts build` - Create the production ready build
- `react-unity-scripts start --test` - Start the test server (entry file will be `test.ts` instead of `index.ts`)

## Extra Environment Variables

- `FILENAME` - Name of the generated javascript file. `index.js` by default.
- `BUILD_DIR` - Path to the generated output. Relative to the project. `../Assets/Resources/react` by default.
- `GENERATE_SOURCEMAP` - `false` by default.
- `HARD_RELOAD` - Reload the entire UI instead of doing HMR. `false` by default.
- `IMAGE_INLINE_SIZE_LIMIT` - `0` by default. Because non-inlined images will be faster in Unity. However, if users still want to inline images, they should increase this limit.

Environment variables can also be defined by having `.env`, `.env.local`, `.env.<development|production>` in project folder.

Custom environment variables are also possible as in [CRA](https://create-react-app.dev/docs/adding-custom-environment-variables).

## WebGL Inspector

When dev server is started with the `start` script, a web server is launched at the selected port (e.g. http://localhost:3000). This server serves the javascript and asset files that are used by ReactUnity. If you visit this link in browser, you will see a prebuilt Unity application that renders your React code. This application can be used to quickly test the React code without even launching Unity. It also reacts to the changes in code by utilizing HMR.

Note that this web inspector has very limited capabilities. However it is a useful tool for when starting a new ReactUnity project. As an advanced feature, you can override the web inspector by placing your custom web inspector in `public` folder under your React project.
