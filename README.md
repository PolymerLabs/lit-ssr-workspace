# lit-ssr-workspace
A workspace for working on lit-ssr and related projects

This repo uses [git submodules](https://git-scm.com/book/en/v2/Git-Tools-Submodules) to check out the following repos/branches:

* PolymerLabs/lit-ssr master
* Polymer/lit-html hydration
* Polymer/lit-element hydration
* webcomponents/template-shadowroot master

Then it uses lerna to treat the submodule directories like packages in a lerna monorepo so that we can run commands across all the repos install dependencies, link the repos together, and build them.

## Getting Started

To get started:

```bash
npm iq
npm run bootstrap
npm run build
```

To lauch the simplistic lit-ssr demo and make sure things are working:
```bash
cd lit-ssr
npm start
```

## Updating the Submodules

See the git submodule docs on [Pulling Upstream Changes from the Project Remote](https://git-scm.com/book/en/v2/Git-Tools-Submodules#_pulling_upstream_changes_from_the_project_remote).

`git pull` on the superproject doesn't update the submodules by default. You need to run:

```bash
git submodule update --init --recursive
```

to recursively fetch and update submodules.

You can configure `git pull` to do this automatically:
```bash
git config submodule.recurse true
```

## Pushing Change to Submodules
See the git submodule docs on [Working on a Submodule](https://git-scm.com/book/en/v2/Git-Tools-Submodules#_working_on_a_submodule).

_TBD_
