## Semantic Versioning

- [Semantic Versioning Cheatsheet](https://devhints.io/semver)

NPM uses semantic versioning to determine which package version to install. NPM will install the latest version that satisfies the semantic versioning rule declared in package.json.

## Semantic Versioning - Major.Minor.Patch

- Major: Breaking changes
- Minor: New features
- Patch: Bug fixes

## Semantic Versioning - Asterisk Tilde and Caret

- Tilde: ~1.2.3 will install the latest patch version of 1.2.x
- Caret: ^1.2.3 will install the latest minor version of 1.x.x
- Asterisk: \* will install the latest version of the package (potentially breaking your code)

## NPM Commands

### Common Commands

- `npm -v` - check npm version
- `npm -h` - list all npm commands
- `npm help <command>` - get help for a specific command
- `npm init --yes` - create a package.json file with default values
- `npm init` - create a package.json file

### Install Packages

- `npm install` - install all dependencies from package.json
- `npm install <package-name>` - install a package and add it to package.json
- `npm install <package-name> --save-dev` - install a package and add it to package.json under devDependencies
- `npm install <package-name> --save` - install a package and add it to package.json under dependencies
- `npm install <package-name>@<version>` - install a specific version of a package
- `npm install <package-name> -g` - install a package globally
- `npm install <package-name> --no-save` - install a package without adding it to package.json
- `npm install <package-name> --no-save --no-package-lock` - install a package without adding it to package.json and without creating a package-lock.json file

### Uninstall Packages

- `npm uninstall <package-name>` - uninstall a package and remove it from package.json
- `npm uninstall <package-name> --save-dev` - uninstall a package and remove it from package.json under devDependencies
- `npm uninstall <package-name> --save` - uninstall a package and remove it from package.json under dependencies
- `npm uninstall <package-name> -g` - uninstall a package globally
- `npm rm <package-name>` - uninstall a package and remove it from package.json
- `npm prune` - remove packages not listed in package.json
- `npm prune --production` - remove packages not listed in package.json under dependencies

### Update Packages

- `npm update` - update all packages listed in package.json
- `npm update <package-name>` - update a package
- `npm update <package-name> --save-dev` - update a package and update package.json under devDependencies
- `npm update <package-name> --save` - update a package and update package.json under dependencies
- `npm update -g` - update all global packages
- `npm outdated` - check for outdated packages
- `npm outdated -g --depth=0` - check for outdated global packages

### List Packages

- `npm list` - list all installed packages
- `npm list --depth=0` - list all installed packages without dependencies
- `npm list --global true --depth=0` - list all installed global packages without dependencies
- `npm list --json` - list all installed packages in json format

### Package Scripts

- `npm run <script-name>` - run a script from package.json
- `npm run` - list all scripts from package.json

### Package Information

- `npm cache clean --force` - clean npm cache
- `npm cache verify` - verify npm cache
- `npm cache ls` - list npm cache
- `npm cache ls --json` - list npm cache in json format

### Config

- `npm config list` - list npm config
- `npm config list --json` - list npm config in json format
- `npm config get <key>` - get a specific npm config
- `npm config set <key> <value>` - set a specific npm config
- `npm config delete <key>` - delete a specific npm config

### Config Global (Author, License, Version, Etc.)\

- `npm set init.author.name "<name>"` - set author name
- `npm set init.author.email "<email>"` - set author email
- `npm set init.author.url "<url>"` - set author url
- `npm set init.license "<license>"` - set license
- `npm set init.version "<version>"` - set version

### Audit

- `npm audit` - audit installed packages
- `npm audit --json` - audit installed packages in json format
- `npm audit fix` - fix vulnerabilities in installed packages
- `npm audit fix --force` - fix vulnerabilities in installed packages (force)

### Publish

- `npm publish` - publish a package
- `npm publish --access public` - publish a public package
- `npm publish --access restricted` - publish a private package
