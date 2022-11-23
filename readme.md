# Multi Env Build Generator

> Building with multiple env files without being restructed to the default .env structure. Allow much more flexibility

## **Build**

2.  Create your environnement project structure under the config folder ⚠️All environnement variables MUST strat with `VITE_`
3.  Add the folder path to the [`.gitignore`](./.gitignore). ⚠️**IT WILL CONTAIN ALL SENSITIVE DATA SO DO NOT SKIP THIS STEP**
4.  Look at the [`package.json`](./package.json) file in order to understand the building structure:
    1. You can add as many .env as you wish for, just add `env-cmd -f [path]`before the `vite build` command below

```bash
npm exec env-cmd -f [path] env-cmd -f [path] vite build
```

## Preview

1.  Preview the build on different environments with `npm run preview`.

## **Local**

If you want to run directly from cli without building the application use : `npm exec -- env-cmd -f ./config/env/.env.dev env-cmd -f ./config/maison/.env.maison.iwc vite`
