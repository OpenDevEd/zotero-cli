# zotero-cli
## Introduction: Tools for working with the APIs of Zotero and Zenodo (zotzen)

This repository is part of a set of repositories, see here: https://github.com/orgs/OpenDevEd/teams/zotzen-team/repositories. Currently, this set contains a number of libraries
- zenodo-lib https://github.com/opendeved/zenodo-lib, https://www.npmjs.com/package/zenodo-lib
- zotero-lib https://github.com/opendeved/zotero-lib, https://www.npmjs.com/package/zotero-lib
- zotzen-lib https://github.com/opendeved/zotzen-lib, https://www.npmjs.com/package/zotzzen-lib

The set contains some command-line tools:
- zenodo-cli https://github.com/opendeved/zenodo-cli, https://www.npmjs.com/package/zenodo-cli
- zotero-cli  https://github.com/opendeved/zotero-cli, https://www.npmjs.com/package/zotero-cli
- zotzen-cli  https://github.com/opendeved/zotzen-cli, https://www.npmjs.com/package/zotzen-cli

And a web application
- zotzen-web https://github.com/opendeved/zotzen-web

# zotero-cli

A commandline tool to interact with the Zotero API. Developed by [@bjohas](https://github.com/bjohas), [@retorquere](https://github.com/retorquere) and [@a1diablo](https://github.com/a1diablo).

Install this tool via
```
npm install -g zotero-cli
```

This tool primarily parses the commandline option, while the API calls are made with https://github.com/OpenDevEd/zotero-api-lib-ts.

## Installation from source
### node

Run the following command to install dependencies

```
npm install
```

Then run to run the script:

```
npm start -- <your args>
```

E.g.

```
npm start -- tags --count
```

#### For compiled JS:

```
npm i @types/node
npm run build
```

Then:

```
./bin/zotero-cli.js <your args>
```

E.g.

```
./bin/zotero-cli.js tags --count
```

## Documentation - overview

### Configuration

Get help with

```
zotero-cli -h
```

Optional arguments:

```
  -h, --help            Show this help message and exit.
  --api-key API_KEY
  --config CONFIG
  --user-id USER_ID
  --group-id GROUP_ID
  --indent INDENT
```

You can create a config.toml file as follows

```
api-key = "..."
group-id = 123
library-type = "group"
indent = 4
```

A file called zotero-cli.toml is picked up automatically.

### Commands

Get help with

```
zotero-cli -h
```

which returns a set of commands, such as key, collection, collections, items, item, publications, trash, tags, searches, attachment, types, fields. You can get help on any of these with

```
zotero-cli <command> --help
```

e.g.

```
zotero-cli collection --help
```

