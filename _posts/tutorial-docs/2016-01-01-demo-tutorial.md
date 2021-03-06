---
title: Demo Tutorial In Atom
link: demo-tutorial
file: 2016-01-01-demo-tutorial.md
categories:
- tutorial-docs
---

### Demoing Your Tutorial

Open a new directory for demoing your tutorial. Setup a new NPM project file.

    > npm init

Add your package name to the `dependencies` in `package.json`:

```json
{
  "dependencies": {
      "coderoad-$YOUR-PACKAGE-NAME$": "^0.1.0"
  }
}
```

Normally you would use `> npm install` to install the package, but your package isn't ready to be published yet. Instead, you need to *"link"* your tutorial package to your demo directory.

### Link Your Demo & Tutorial

[NPM link](https://docs.npmjs.com/cli/link) creates a symbolic link between directories. This allows your demo directory to always load your tutorial package.

Inside of your tutorial root directory, run npm link.

    > npm link

Inside of your demo root directory, connect the link.

    > npm link coderoad-$YOUR-PACKAGE-NAME$
    > npm install


### Using Atom

Use [*Builder-CodeRoad*](/builder-coderoad.html) to develop your tutorial. Builder-CodeRoad allows you to visualize and test your tutorial as you develop it.

When it's ready, you can play your tutorial in *Atom-Coderoad*. Your package should appear as a loaded package. Click on it.

If you make any changes to your tutorial, you'll have to reload *Atom* to view them. You can use the Atom [command-palette](https://atom.io/docs/latest/getting-started-atom-basics#command-palette) to find "reload" or simply use the reload hot-key (*Windows & Linux*: alt-ctrl-r, *Mac*: ctrl-alt-cmd-l).
