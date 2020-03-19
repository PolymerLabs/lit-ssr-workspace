# lit-ssr-workspace
A workspace for working on lit-ssr and related projects

This repo uses git submodules to check out the following repos/branches:

* PolymerLabs/lit-ssr master
* Polymer/lit-html hydration
* Polymer/lit-element hydration
* webcomponents/template-attach-shadow master

Then is uses lerna to treat the submodule directories like packages in a lerna monorepo so that we can run commands across all the repos install dependencies, link the repos together, and build them.

To get started:

```bash
npm i
npm run bootstrap
npm run build
```

To lauch the simplistic lit-ssr demo and make sure things are working:
```bash
cd lit-ssr
npm start
```

To do work in these submodules requires a little git submodule knowledge. Instructions forthcoming.
