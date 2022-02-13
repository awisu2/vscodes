# settings

- *.vscode/settings.json*: プロジェクト固有の設定が反映

```bash
mkdir .vscode
echo "{}" > .vscode/settings.json
```

## 基本

まずはこれを記載、その上で必要な言語用設定を追加
editor.formatOnSave 以外は、user の settings に書いてもいいかも

```json
{
  "editor.tabSize": 2,
  // 改行コード
  "files.eol": "\n",
  // コマンドプロンプト
  "[bat]": {
    "files.encoding": "shiftjis",
    "files.eol": "\r\n"
  },
  // prettierである必要はない。これを指定しないとformatOnSaveがうまく動作しないっぽい
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true
}
```

## html

prettier だと余計な挙動をするのデフォルトでまかなう

```json
{
  // html
  "html.format.endWithNewline": true,
  "html.format.indentInnerHtml": false,
  "html.format.maxPreserveNewLines": 1,
  "html.format.wrapAttributes": "auto",
  "html.format.wrapLineLength": 88,
  "html.format.preserveNewLines": true,
  "[html]": {
    "editor.defaultFormatter": "vscode.html-language-features"
  }
}
```

## javascript, json, typescript , typescriptreact

拡張の prettier を利用

```json
{
  // javascript, json, typescript , typescriptreact
  // 88の意味はあまりない。htmlに合わせた
  "prettier.printWidth": 88,
  "prettier.tabWidth": 2,
  "prettier.semi": false,
  "prettier.singleQuote": true,
  // {}や()の内部変数の前後へのスペース付与フラグ
  "prettier.bracketSpacing": true,
  // 改行コード
  "prettier.endOfLine": "lf",
  // 最後の,を強制
  "prettier.trailingComma": "none",
  // scriptなどのタグ内で、indentをつけない
  "prettier.vueIndentScriptAndStyle": false,

  // prettierの対象外とする拡張子
  "prettier.disableLanguages": [],
  // ignore対象設定ファイル
  "prettier.ignorePath": ".prettierignore"
}
```

## python

formatter は black。flex8, mypy を有効にして、pylint は停止、black に合わせるため、少し flake8 を調整。
flake8 で都合の悪いエラーが出たら、link のチートシートで調べる
後半の test の部分はおまけ

**Pylance** 拡張をインストールすると syntax hilight (import や error など) でわかりやすくなる

_.vscode/extensions.json_

```json
{
  "recommendations": ["ms-python.python", "ms-python.vscode-pylance"]
}
```

```json
{
  // python
  "python.venvPath": ".venv",
  // windowsだとどうしても.exeがついてしまい、変更が発生してしまう。(workspaceに指定するのが良いかもしれない)
  // "python.pythonPath": ".venv\\Scripts\\python.exe",

  // formatter
  "python.formatting.provider": "black",

  // flex8, mypyを有効にして、pylintは停止、blackに合わせるため、少しflake8を調整
  "python.linting.pylintEnabled": false,
  "python.linting.mypyEnabled": true,
  "python.linting.lintOnSave": true,
  "python.linting.flake8Enabled": true,
  "python.linting.flake8Args": ["--max-line-length=88"],
  // test系(おまけで設定)
  "python.testing.unittestArgs": ["-v", "-s", "./tests", "-p", "test_*.py"],
  "python.testing.pytestEnabled": false,
  "python.testing.nosetestsEnabled": false,
  "python.testing.unittestEnabled": true,
  "[python]": {
    "editor.defaultFormatter": "ms-python.python"
  }
}
```

## shell

```json
{
  // shell
  "[shellscript]": {
    "editor.defaultFormatter": "foxundermoon.shell-format"
  }
}
```
