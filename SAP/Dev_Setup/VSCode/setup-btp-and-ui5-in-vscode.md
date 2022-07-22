# Setup VSCode for BTP and UI5 Development

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/VSCode/images/vscodebtpui5.png"  width="15%">

### References

### CAP/UI5

- [CAP - VSCode Tools](https://cap.cloud.sap/docs/tools/#vscode)
- [CAP DevTut - VSCode setup](https://developers.sap.com/tutorials/btp-app-set-up-local-development.html)

- [UI5 - VSCode Tools](https://blogs.sap.com/2021/10/15/getting-ready-for-ui5-development-with-visual-studio-code/)
- [UI5 Tooling - Getting Started](https://sap.github.io/ui5-tooling/pages/GettingStarted/)

### Tooling

- [Installing Node, NPM, NVM](https://docs.npmjs.com/downloading-and-installing-node-js-and-npm)
- [Update Node Version](https://phoenixnap.com/kb/update-node-js-version)
- [NVM Reference](evernote:///view/22287029/s194/57aceb2f-260d-4ba7-97f6-9764607cbb96/9726ee1c-1a28-4702-8053-96e8e6e6faf7/)
- [Cloud MTA Build Tool](https://sap.github.io/cloud-mta-build-tool/download/)
- [VSCode MTA Tools](https://github.com/SAP/vscode-mta-tools)

* * * * *

### Git

- [Download Git](https://git-scm.com/downloads)
- [What is Git?](https://git-scm.com/book/en/v2/Getting-Started-What-is-Git%3F)
- [VS Code version control Git support](https://code.visualstudio.com/docs/editor/versioncontrol#_git-support)

```bash
git version
```

### Node/NPM

```bash
node --version      # what node installed

nvm --version       # what nvm installed

nvm ls              # what version currently in use

nvm ls-remote       # is a newer version available

nvm install --lts   # install latest version
nvm install x.x.x   # install specific version 

nvm use x.x.x       # switch to version
```

### CloudFoundry

```bash
cf --version

brew --version

brew install cloudfoundry/tap/cf-cli
```

### CDS

```bash
cds --version
```

### Cloud MTA Build Tool

- [The Multi-Target Model](https://www.sap.com/documents/2016/06/e2f618e4-757c-0010-82c7-eda71af511fa.html)

- Standalone cmd-line tool
- Builds a _Multi-Target Application (MTA)_ archive &#10148; _.mtarfile_
- Is deployment-ready
- Built from MTA project artefacts, from either:
  - A project's MTA development descriptor &#10148; mta.yamlfile
  - Module build artefacts as-per MTA deployment descriptor &#10148; mtad.yamlfile
- Archive builder used on file system independent of dev env where app project created

```bash
npm install --global gnumake

npm install -g mbt

cf install-plugin multiapps # Multiapps plugin for MTA

npm install -g mta
```

### VSCode

- F1 &#10148; _shell command_ &#10148; _Install 'code' command in PATH_
- Add Extensions

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/VSCode/images/ui5tools.png"  width="45%">

- For UI5 development

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/VSCode/images/ui5langassist.png"  width="45%">

### Yeoman &#10148; UI5 Development

```bash
yo --version

npm install -g yo

npm install -g generator-easy-ui5 
```

- Use _F1 ➤ Fiori: Open Application Generator_ to quick start UI5

### UI5 Tooling &#10148; UI5 Cli

```bash
ui5 --version

npm install -g @ui5/cli
```

### UI5 Bootstrapping &#10148; New Project

- See the [UI5 Tooling Getting Started](https://sap.github.io/ui5-tooling/pages/GettingStarted/) page for details
- See [UI5 Tooling - A Modern Development Experience for UI5](https://blogs.sap.com/2020/04/07/ui5-tooling-a-modern-development-experience-for-ui5/)

- Install the @UI5/cli tooling as described above
- To enable an existing project

```bash
npm init --yes          # add package.json

ui5 init                # add ui5.yaml

ui5 use openui5@latest  # add framework
  or
ui5 use sapui5@latest

ui5 add sap.ui.core sap.m sap.ui.table themelib_sap_fiori_3 # [...] // add req'd libraries

ui5 serve               # start the server

ui5 build --all         # build optimised version of project for deployment
```

- Updating Project Dependencies

```bash
npm install -g npm-check-updates

ncu -u

npm install
```

### Add Code Assist via Typescript to UI5 Project

- Per project, add `devDependencies`;

```bash
npm install --save-dev eslint @sap/eslint-plugin-ui5-jsdocs @sapui5/ts-types
```

- Add `tsconfig.json` to project root to use UI5 types

```json
{
  "compilerOptions": {
    "module": "none",
    "noEmit": true,
    "checkJs": true,
    "allowJs": true,
    "types": [
      "@sapui5/ts-types"
    ]
  }
}
```

- To make `ESLint` aware of _ui5-jsdocs_ plugin
  - Add `.eslintrc` file to project root (or add to existing file)

```json
{
  "plugins": [
    "@sap/ui5-jsdocs"
  ],
  "extends": [
    "plugin:@sap/ui5-jsdocs/recommended",
    "eslint:recommended"
  ]
}
```

### UI5 - Using a Proxy for Remote Services

- See [UI5 Tooling - A Modern Development Experience for UI5](https://blogs.sap.com/2020/04/07/ui5-tooling-a-modern-development-experience-for-ui5/)
- Using a Proxy (refer to the linked doc above)

```bash
npm install ui5-middleware-simpleproxy --save-dev # auto installed if project gen'd from Yeoman
```

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/VSCode/images/packagejson.png"  width="45%">

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/VSCode/images/ui5yaml.png"  width="45%">

<img src="https://github.com/aawa69/Notes/blob/main/SAP/Dev_Setup/VSCode/images/manifest.png"  width="45%">
