# @womorg/adipisci-enim-illum

[![npm](https://img.shields.io/npm/v/@womorg/adipisci-enim-illum)](https://www.npmjs.com/package/@womorg/adipisci-enim-illum)

`@womorg/adipisci-enim-illum` is a node command line tool to generate directory structure tree.

## Installation

```bash
npm i @womorg/adipisci-enim-illum -g
```

## Usage

```bash
$ @womorg/adipisci-enim-illum -h
Usage: @womorg/adipisci-enim-illum [options]

Generate a directory structure tree

Options:
  -V, --version          output the version number
  -i, --ignore <ig>      ignore specific directory name, separated by comma or '|'  
  -l, --layer <layer>    specify the layer of output
  -d, --directory <dir>  specify the directory to generate structure tree
  -f, --only-folder      output folder only
  --icon                 output emoji icon, prefixing filename or directory
  -o, --output <output>  export content into a file, appending mode by default      
  -h, --help             display help for command
```

## Examples

Ignore `.git` and `node_modules` directory.

```bash
$ @womorg/adipisci-enim-illum -i '.git|node_modules' # or @womorg/adipisci-enim-illum -i '.git,node_modules'
@womorg/adipisci-enim-illum
├──📄.editorconfig
├──📄.eslintrc.js
├──📄.gitignore
├──📄.prettierrc.js
├──📄.release-it.json
├──📄CHANGELOG.md
├──📄LICENSE
├──📄package-lock.json
├──📄package.json
├──📄README.md
└──📁src
    ├──📄config.js
    ├──📄generate.js
    ├──📄index.js
    ├──📄toTree.js
    └──📄utils.js
```

Show emoji icon, prefixing filename or directory.

```bash
$ @womorg/adipisci-enim-illum -i '.git,node_modules' --icon
@womorg/adipisci-enim-illum
├──📄.editorconfig
├──📄.eslintrc.js
├──📄.gitignore
├──📄.prettierrc.js
├──📄.release-it.json
├──📄CHANGELOG.md
├──📄LICENSE
├──📄package-lock.json
├──📄package.json
├──📄README.md
└──📁src
    ├──📄config.js
    ├──📄generate.js
    ├──📄index.js
    ├──📄toTree.js
    └──📄utils.js
```

Export output into `result.md`, and append mode by default.

```bash
$ @womorg/adipisci-enim-illum -i '.git,node_modules' -o result.md
@womorg/adipisci-enim-illum
├──📄.editorconfig
├──📄.eslintrc.js
├──📄.gitignore
├──📄.prettierrc.js
├──📄.release-it.json
├──📄CHANGELOG.md
├──📄LICENSE
├──📄package-lock.json
├──📄package.json
├──📄README.md
└──📁src
    ├──📄config.js
    ├──📄generate.js
    ├──📄index.js
    ├──📄toTree.js
    └──📄utils.js
```
## License

[MIT](./LICENSE)
