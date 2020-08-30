<p align="center">
<img width="500px" src="https://raw.githubusercontent.com/ijsto/eslint-config/master/img/jumbo-v2.png"/>
</p>

# ESLint and Prettier configs for Next.js apps

A set of awesome ESLint + Prettier configs.
Makes it easier to work with React, NextJS, Node apps.

This package is intended for use with VS Code, however, can be easily used with any text editors.

# Installation

First installation will take you only a couple of minute, every subsequent should not take more than a minute.

You can install the package 2.a) in repo of the project which will apply the linting only to the project and not other files on your computer or 2.b) on your computer which will apply the linting to all files with the included file extensions on your computer.

Below are the steps to install (click on the step to open the instructions).

<details><summary><span>1 · VS Code Setup</span></summary>
<p>
Set up VS Code to fix ESLint issues on save and disable editor formatOnSave action.

1. Install [ESLint extension](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
2. In VS Code go to settings (`⌘Cmd + ,` or `Ctrl + ,`) → type in `settings.json` file → click on `Edit in settings.json` and paste in the following on the root of the object:

```js
{
  // ...
  // Run formatter when you save code changes
  "editor.formatOnSave": true,
  // Disable default formatting (ESLint formatting will be used instead)
  "[javascript]": {
    "editor.formatOnSave": false
  },
  "[javascriptreact]": {
    "editor.formatOnSave": false
  },
  // Auto-fix issues with ESLint when you save code changes
  "editor.codeActionsOnSave": {
      "source.fixAll.eslint": true
  },
  // Prevent double-formatting and potential ESLint <> Prettier conflicts (ESLint formatting will be used instead)
  "prettier.disableLanguages": [
      "javascript",
      "javascriptreact",
      "typescript",
      "typescriptreact",
  ],
}
```

</p>
</details>

<details><summary><span>2.a · Per Project Setup (Local setup)</span></summary>
<p>

1. Install @ijsto/eslint-config:

```
npx install-peerdeps --dev @ijsto/eslint-config
```

2. Create an `.eslintrc` file in the root of your project's directory. Paste in the following:

```json
{
  "extends": "@ijsto"
}
```

3. You're done!

4. ESLint will run each time you save your file changes.

### Uninstall

This command will uninstall the @eslint-config and all related devDependencies **locally** (from the project)

If you have installed any of the eslint-config or eslint-plugin packages separately, don't forgot to remove it from the list.

```
yarn remove @ijsto/eslint-config @prisma/cli babel-eslint eslint eslint-config-airbnb eslint-config-prettier eslint-plugin-html eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks prettier
```

```
npm --global @ijsto/eslint-config @prisma/cli babel-eslint eslint eslint-config-airbnb eslint-config-prettier eslint-plugin-html eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks prettier
```

</p>
</details>
<h3 style="margin: 1rem">
or
</h3>

<details><summary><span>2.b · Computer-wide (Global setup)</span></summary>
<p>

If you would like to install the config computer-wide (globally) and not on each project, follow the below steps.
There are some caveats to this setup.

1. Install @ijsto/eslint-config:

```
npx install-peerdeps --global @ijsto/eslint-config
```

2. Create a global `.eslintrc` file on your computer:

- MacOS location: `~/.eslintrc`
- Windows location: `C:\Users\you\.eslintrc`

Paste in the follow to newly created `.eslintrc`:

```json
{
  "extends": "@ijsto"
}
```

### Uninstall globally

This command will uninstall the @eslint-config and all related devDependencies **globally** (from your computer)

If you have installed any of the eslint-config or eslint-plugin packages separately, don't forgot to remove it from the list.

```
yarn global remove @ijsto/eslint-config @prisma/cli babel-eslint eslint eslint-config-airbnb eslint-config-prettier eslint-plugin-html eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks prettier
```

```
npm remove --global @ijsto/eslint-config @prisma/cli babel-eslint eslint eslint-config-airbnb eslint-config-prettier eslint-plugin-html eslint-plugin-import eslint-plugin-jsx-a11y eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks prettier
```

</p>
</details>

<hr style="margin: 1rem"/>

## That's all.

Did this package help you? Give it a ★ and share with your friends! 🙂

PRs, feature requests or suggestions are most welcome!

[iJS.to](https://ijs.to)
