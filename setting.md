# vscode 设置

```json
{
  // 编辑器设置
  "editor.renderIndentGuides": false,
  "locale": "zh-CN", // 语言
  "editor.tabSize": 2, // 缩进
  "editor.formatOnSaveTimeout": 500,
  // 代码自动格式化
  "editor.formatOnPaste": true,
  "editor.formatOnSave": true,
  "editor.formatOnType": true,
  // 主题
  "workbench.colorTheme": "SynthWave '84",
  // custome js and css 自定义样式
  "vscode_custom_css.imports": [
    "file:///D:/web/vscode-third-dev/synthwave/synthwave84.css"
  ],
  // 字体
  // "editor.fontFamily": "Fira Code",
  "editor.fontLigatures": true,
  "editor.fontSize": 14,
  "editor.fontWeight": "normal",
  // 文件图标
  "workbench.iconTheme": "vscode-icons",
  // 终端
  "terminal.integrated.shell.windows": "C:\\Windows\\System32\\cmd.exe",
  // 背景图
  "backgroundCover.randomImageFolder": "d:\\素材模版\\背景图",
  "backgroundCover.autoStatus": false,
  "backgroundCover.imagePath": "d:\\素材模版\\背景图\\12987.jpg",
  "backgroundCover.opacity": 1,
  // git
  "git.confirmSync": false,
  "gitlens.advanced.messages": {
    "suppressFileNotUnderSourceControlWarning": true,
    "suppressLineUncommittedWarning": true
  },
  // Vetur配置
  "vetur.format.defaultFormatterOptions": {
    "prettier": {
      "semi": false, // 格式化不加分号
      "singleQuote": true // 格式化以单引号为主
    }
  },
  //分号和双引号确实不会再自动添加了，但是不会在方法括号之间插入空格，可以再加入这条配置即可
  "javascript.format.insertSpaceBeforeFunctionParenthesis": true,
  "vetur.format.defaultFormatter.js": "vscode-typescript",
  // prettier配置文件
  "prettier": {
    "printWidth": 80,
    "tabWidth": 2,
    "useTabs": false,
    "singleQuote": true,
    "semi": false,
    "trailingComma": "none",
    "bracketSpacing": true
  },
  // "prettier.configPath": "D:\\web\\vscode-third-dev\\.prettierrc",
  // eslint配置
  "eslint.autoFixOnSave": true,
  "eslint.alwaysShowStatus": true,
  "eslint.options": {
    "extensions": [".html", ".js", ".vue", ".jsx"]
  },
  // wepy
  "files.associations": {
    "*.cjson": "jsonc",
    "*.wxss": "css",
    "*.wxs": "javascript",
    "*.vue": "vue",
    "*.wpy": "vue"
  },
  "emmet.includeLanguages": {
    "wxml": "html"
  },
  // code-runner
  "code-runner.executorMap": {
    "python": "python3 -u"
  },
  "code-runner.defaultLanguage": "python",
  "code-runner.runInTerminal": true,
  "code-runner.clearPreviousOutput": true,
  // 默认格式化工具
  "git.enableSmartCommit": true,
  "[javascript]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "[vue]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  }
}
```

# eslint

[eslint 常用配置项](./eslint.md)

## .eslintrc.js 配置

```json
(module.exports = {
  "root": true,
  "env": {
    "node": true
  },
  "extends": ["plugin:vue/essential", "@vue/prettier"],
  "rules": {
    "no-console": process.env.NODE_ENV === "production" ? "error" : "off",
    "no-debugger": process.env.NODE_ENV === "production" ? "error" : "off",
    "prettier/prettier": "error"
  },
  "parserOptions": {
    "parser": "babel-eslint"
  }
})
```

# Prettier

## 一共有三种方式支持对 Prettier 进行配置：

1. 根目录创建.prettierrc 文件，能够写入 YML、JSON 的配置格式，并且支持.yaml/.yml/.json/.js 后缀；
2. 根目录创建.prettier.config.js 文件，并对外 export 一个对象；
3. 在 package.json 中新建 prettier 属性。

### .prettierrc 配置

```json
{
  "printWidth": 80,
  "tabWidth": 2,
  "useTabs": false,
  "singleQuote": true,
  "semi": false,
  "trailingComma": "none",
  "bracketSpacing": true
}
```

[prettier 官网配置项](https://prettier.io/docs/en/options.html)
