# shortcut

- settings: `ctrl + ,`

## recomends

- **new file** with shortcut
  - can't user on browser version
  - links
    - [VS Code \- Add a new file under the selected working directory \- Stack Overflow](https://stackoverflow.com/questions/39599514/vs-code-add-a-new-file-under-the-selected-working-directory)
    - [VSCode \- Create Files and Folders without using mouse \- DEV Community](https://dev.to/equiman/vscode-create-files-and-folders-on-the-go-2hd6)
  - <details>
      <summary>setting description</summary>

      *keybindings.json*
      ```json
      [
          {
              "key": "ctrl+n",
              "command": "explorer.newFile",
              "when": "explorerViewletFocus"
          },
          {
              "key": "ctrl+shift+n",
              "command": "explorer.newFolder",
              "when": "explorerViewletFocus"
          },
          // on windows/linux
          {
            "key": "ctrl+shift+n",
            "command": "workbench.action.newWindow",
            "when": "!explorerViewletFocus"
          }
      ]
      ```

    </details>

## note


## edit shortcuts

[Visual Studio Code Key Bindings](https://code.visualstudio.com/docs/getstarted/keybindings)

- open gui: `ctrl + shift + p` > *Preferences: Open Keyboard Shortcuts*
  - open json: `ctrl + shift + p` > *Preferences: Open Keyboard Shortcuts (JSON)*
  - open help: `ctrl + shift + p` > *Help: Shortcuts Reference*
- json: [Visual Studio Code Key Bindings](https://code.visualstudio.com/docs/getstarted/keybindings#_advanced-customization)
  - name: **keybindings.json** ユーザ設定でのみ可能(みたい)


