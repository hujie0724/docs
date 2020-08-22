# 目录

- 环境安装
  - [工具包管理](#工具包管理)
  - [Node](#node)
  - [Git](#git)
  - [Git 图形操作工具（GitKraken）](#gitkraken)
  - [终端工具](#终端工具)
- 环境配置
  - [终端切换](#终端工具)
  - [Git 全局配置](#Git-全局配置)
  - [VSCode](#vscode)
    - 插件
    - 配置
  - [小程序编辑器](#小程序编辑器)
    - 插件
    - 配置

## 工具包管理

|    系统 | 工具                                     |
| ------: | :--------------------------------------- |
|     Mac | [Homebrew](https://brew.sh)              |
| Windows | [Chocolatey](https://www.chocolatey.org) |

## Node

|    系统 | 工具                   |                                                                   |
| ------: | :--------------------- | :---------------------------------------------------------------- |
|     Mac | `brew install node`    | ![homebrew](https://img.shields.io/homebrew/v/node)               |
| Windows | `choco install nodejs` | ![Chocolatey Version](https://img.shields.io/chocolatey/v/nodejs) |

## Git

|    系统 | 工具                | 版本                                                           |
| ------: | :------------------ | :------------------------------------------------------------- |
|     Mac | `brew install git`  | ![homebrew](https://img.shields.io/homebrew/v/git)             |
| Windows | `choco install git` | ![Chocolatey Version](https://img.shields.io/chocolatey/v/git) |

## GitKraken

|    系统 | 工具                                                                                                                                       |
| ------: | :----------------------------------------------------------------------------------------------------------------------------------------- |
|     Mac | [GitKraken](https://release.gitkraken.com/darwin/installGitKraken.dmg)                                                                     |
| Windows | GitKraken [64bit](https://release.gitkraken.com/win64/GitKrakenSetup.exe)，[32bit](https://release.gitkraken.com/win32/GitKrakenSetup.exe) |

## 终端工具

|    系统 | 工具                             |                           |
| ------: | :------------------------------- | :------------------------ |
|     Mac | [iTerm2](https://www.iterm2.com) |                           |
| Windows | `Git Bash`                       | 👈 安装`Git`工具后即可使用 |

## 命令终端工具切换

> 用于 Mac 环境

| 终端 | 命令                |        |
| ---: | :------------------ | :----- |
|  zsh | `chsh -s /bin/zsh`  | 👈 推荐 |
| bash | `chsh -s /bin/bash` |        |

## Git-全局配置

```shell
# 设置用户名
git config --global user.name [xxx]

# 设置邮箱
git config --global user.email [xxx@xxx.xxx]

# 显示颜色
git config --global color.ui true

# 默认推送当前分支
git config --global push.default current

# 拉取远程分支时，是否使用快速合并
git config --global pull.ff false

# 拉取远程分支时，是否保持提交曲线为直线
git config --global pull.rebase true
```

## VSCode

- 插件
  |                                                                                                    插件 | 版本                                                                                                                                                                                                                                                                                                                       |
  | ------------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
  |                      [Easy LESS](https://marketplace.visualstudio.com/items?itemName=mrcrowl.easy-less) | [![](https://vsmarketplacebadge.apphb.com/version/mrcrowl.easy-less.svg)](https://marketplace.visualstudio.com/items?itemName=mrcrowl.easy-less) [![](https://vsmarketplacebadge.apphb.com/installs/mrcrowl.easy-less.svg)](https://marketplace.visualstudio.com/items?itemName=mrcrowl.easy-less)                         |
  |                     [minapp](https://marketplace.visualstudio.com/items?itemName=qiu8310.minapp-vscode) | [![](https://vsmarketplacebadge.apphb.com/version/qiu8310.minapp-vscode.svg)](https://marketplace.visualstudio.com/items?itemName=qiu8310.minapp-vscode) [![](https://vsmarketplacebadge.apphb.com/installs/qiu8310.minapp-vscode.svg)](https://marketplace.visualstudio.com/items?itemName=qiu8310.minapp-vscode)         |
  | [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) | [![](https://vsmarketplacebadge.apphb.com/version/esbenp.prettier-vscode.svg)](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) [![](https://vsmarketplacebadge.apphb.com/installs/esbenp.prettier-vscode.svg)](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)     |
  |                               [Vetur](https://marketplace.visualstudio.com/items?itemName=octref.vetur) | [![](https://vsmarketplacebadge.apphb.com/version/octref.vetur.svg)](https://marketplace.visualstudio.com/items?itemName=octref.vetur) [![](https://vsmarketplacebadge.apphb.com/installs/octref.vetur.svg)](https://marketplace.visualstudio.com/items?itemName=octref.vetur)                                             |
  |           [Vue 2 Snippets](https://marketplace.visualstudio.com/items?itemName=hollowtree.vue-snippets) | [![](https://vsmarketplacebadge.apphb.com/version/hollowtree.vue-snippets.svg)](https://marketplace.visualstudio.com/items?itemName=hollowtree.vue-snippets) [![](https://vsmarketplacebadge.apphb.com/installs/hollowtree.vue-snippets.svg)](https://marketplace.visualstudio.com/items?itemName=hollowtree.vue-snippets) |

- 配置
  <details>
  <summary><mark><font color=red>>>>点击展开<<<</font></mark></summary>

  ```json
  {
    "editor.formatOnSave": true,
    "editor.stablePeek": true,
    "editor.tabCompletion": "on",
    "editor.tabSize": 2,
    "editor.wordWrapColumn": 120,
    "editor.minimap.enabled": false,
    "explorer.openEditors.visible": 0,
    "search.exclude": {
      "**/dist": true,
      "**/miniprogram_npm": true
    },
    "files.watcherExclude": {
      "**/dist/**": true,
      "**/miniprogram_npm/**": true
    },
    "files.associations": {
      "*.cjson": "jsonc",
      "*.wxs": "javascript",
      "*.wxss": "css"
    },
    "emmet.includeLanguages": {
      "wxml": "html"
    },
    "minapp-vscode.wxmlFormatter": "prettyHtml",
    "minapp-vscode.formatMaxLineCharacters": 120,
    "minapp-vscode.disableAutoConfig": true,
    "minapp-vscode.showSuggestionOnEnter": true,
    "minapp-vscode.prettier": {
      "printWidth": 120,
      "semi": false,
      "singleQuote": true,
      "trailingComma": "none"
    },
    "minapp-vscode.prettyHtml": {
      "printWidth": 120,
      "usePrettier": false,
      "sortAttributes": true
    },
    "vetur.format.defaultFormatterOptions": {
      "prettyhtml": {
        "printWidth": 120,
        "usePrettier": false,
        "sortAttributes": true
      },
      "prettier": {
        "printWidth": 120,
        "semi": false,
        "singleQuote": true,
        "trailingComma": "none"
      }
    },
    "prettier.printWidth": 120,
    "prettier.singleQuote": true,
    "prettier.semi": false,
    "prettier.trailingComma": "none",
    "less.compile": {
      "outExt": ".wxss"
    }
  }
  ```
  </details>

## 小程序编辑器

- 插件
  |                                                                                                    插件 | 版本                                                                                                                                                                                                                                                                                                                   |
  | ------------------------------------------------------------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
  |                      [Easy LESS](https://marketplace.visualstudio.com/items?itemName=mrcrowl.easy-less) | [![](https://vsmarketplacebadge.apphb.com/version/mrcrowl.easy-less.svg)](https://marketplace.visualstudio.com/items?itemName=mrcrowl.easy-less) [![](https://vsmarketplacebadge.apphb.com/installs/mrcrowl.easy-less.svg)](https://marketplace.visualstudio.com/items?itemName=mrcrowl.easy-less)                     |
  |                     [minapp](https://marketplace.visualstudio.com/items?itemName=qiu8310.minapp-vscode) | [![](https://vsmarketplacebadge.apphb.com/version/qiu8310.minapp-vscode.svg)](https://marketplace.visualstudio.com/items?itemName=qiu8310.minapp-vscode) [![](https://vsmarketplacebadge.apphb.com/installs/qiu8310.minapp-vscode.svg)](https://marketplace.visualstudio.com/items?itemName=qiu8310.minapp-vscode)     |
  | [Prettier - Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) | [![](https://vsmarketplacebadge.apphb.com/version/esbenp.prettier-vscode.svg)](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) [![](https://vsmarketplacebadge.apphb.com/installs/esbenp.prettier-vscode.svg)](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) |

- 配置
  <details>
  <summary><mark><font color=red>>>>点击展开<<<</font></mark></summary>

  ```json
  {
    "editor.formatOnSave": true,
    "editor.stablePeek": true,
    "editor.tabCompletion": "on",
    "editor.tabSize": 2,
    "editor.wordWrapColumn": 120,
    "editor.minimap.enabled": false,
    "explorer.openEditors.visible": 0,
    "search.exclude": {
      "**/dist": true,
      "**/miniprogram_npm": true
    },
    "files.watcherExclude": {
      "**/dist/**": true,
      "**/miniprogram_npm/**": true
    },
    "files.associations": {
      "*.cjson": "jsonc",
      "*.wxs": "javascript",
      "*.wxss": "css"
    },
    "[wxml]": {
      "editor.defaultFormatter": "qiu8310.minapp-vscode"
    },
    "[css]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[json]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "[javascript]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode"
    },
    "minapp-vscode.wxmlFormatter": "prettyHtml",
    "minapp-vscode.formatMaxLineCharacters": 120,
    "minapp-vscode.disableAutoConfig": true,
    "minapp-vscode.showSuggestionOnEnter": true,
    "minapp-vscode.prettier": {
      "printWidth": 120,
      "semi": false,
      "singleQuote": true,
      "trailingComma": "none"
    },
    "minapp-vscode.prettyHtml": {
      "printWidth": 120,
      "usePrettier": false,
      "sortAttributes": true
    },
    "prettier.printWidth": 120,
    "prettier.singleQuote": true,
    "prettier.semi": false,
    "prettier.trailingComma": "none",
    "less.compile": {
      "outExt": ".wxss"
    }
  }
  ```
  </details>
