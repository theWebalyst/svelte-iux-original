# Svelte iUX - Incremental UX Component Library

WORK IN PROGRESS - nothing to see here!

**Svelte iUX** is a library of experimental web components being used to explore ideas for improving the UX of a complex application: [Visualisation Lab](https://github.com/theWebalyst/visualisation-lab). The components are created for use with the Svelte web framework.

The ideas may well be transferrable, which is one reason these components are in a separate library.

This component library uses **Svench**, an experimental workbench for building Svelte components, and was made by taking a copy of the [svench/example](https://github.com/rixo/svench/tree/master/example) directory and modifying that.

## Using Svench

Svench is at this time still a proof of concept and so subject to change, but some basics
on using it are included below. For latest information on Svench or more details on
the configuration files see the [Svench github](https://github.com/rixo/svench/).

### Prerequisites
- `node` v12

This project has a `.nvmrc` file for use with `nvm` to select `node` version which can be used as below:

### Setup
```bash
git clone https://github.com/theWebalyst/svelte-iux.git
cd svelte-iux
nvm use
yarn
```

### Start Svench

```bash
yarn svench
```

Open http://localhost:4242. Edit / add things in `./src`.

### Using Svench

Each component has a '.svench' file next to the '.svelte' component file, and this file is used by Svench to create its menu, and provide the context for
displaying and interacting with the component.

For more on these, see the [Svench README](https://github.com/rixo/svench/).

## LICENSE
See LICENSE. 

TL;DR:
- **Svelte iUX** Compnents are under GPLv3
