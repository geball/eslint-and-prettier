The following is based off of Wes Bos' guide at https://www.youtube.com/watch?v=lHAeK8t94as 🔥

1. Set up project with `npm init`.
2. Run `npx install-peerdeps --dev eslint-config-wesbos`.
3. Add the enclosed .eslintrc file into the project. Set any disabling rules in .eslintrc as needed.
4. Add the following to "scripts" in package.json:

   ```json
   "lint": "eslint .",
   "lint:fix": "eslint . --fix"
   ```

5. Run `npm run lint:fix`.
6. Install the ESLint package (by Dirk Baeumer) in VS Code.
7. Go to VS Code settings.json and add the following:

   ```json
   "editor.formatOnSave": true,
   "[javascript]": {
   "editor.formatOnSave": false
   },
   "[javascriptreact]": {
   "editor.formatOnSave": false
   },
   "eslint.alwaysShowStatus": true,
   "editor.codeActionsOnSave": {
   "source.fixAll.eslint": true
   },
   "prettier.disableLanguages": ["js"],
   ```

See also https://dev.to/bdesigned/vscode-setup-with-eslint-and-prettier-1gek by Brittney Postma.
