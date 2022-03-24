# on browser

- [default \(Workspace\) \- Visual Studio Code](https://vscode.dev/)
- [Release Notes: 1\.64\.2 \- default \(Workspace\) \- Visual Studio Code](https://vscode.dev/)

## NOTE

- terminalが利用できないため、今の所テキスト編集向け
  - とはいえブックマーク開くだけなのは非常に楽
  - 後述するようにコミットがすぐpushされるのでメモ先としては非常に楽

## What can or cannot be done

latupdate: 2022/03/24
ソースコードはGitHubのリポジトリから取得

- Terminals are not available
  - 開こうとするとローカル環境にコピーを作ってそちらを使ってねと言われる
- ctrlを押しながらのリンク移動は限定的
  - http付きのリンクはok、相対パスは不可
- リポジトリから持ってきた場合
  - ブランチ移動は可能
  - コミットはすぐにpushされる
- 保存がない。編集したら即時確定(保存)している
- Stagingがない、SourceControlで一時的にStaged Changesにあげておいても編集するとChangesとして扱われる
  - 一時的にStaged Changes に残らない
- 拡張や .vscode/settings.json もあんまり効かない
  - 拡張: 制限があるよと言われたり、グレー表示でインストールできなかったり
- コミットしなくても編集状況は残る: どれくらいかはわからない
