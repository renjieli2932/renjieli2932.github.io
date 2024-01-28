---
title: Create VS Code Hotkeys to bold and italic text 
date: 2024-01-28 16:50:00 +/-TTTT
categories: [Tech]
tags: [vscode]     # TAG names should always be lowercase
---

I am using VS Code to manage and write the LaTeX/markdown files. Every time I want to **bold**/*italic* something , I have to manually type commands like \textbf and brackets, which is extremely laborious and meaningless. 

According to the [offical documentation](https://code.visualstudio.com/docs/getstarted/keybindings), we can define the key bindings by ourselves.

Basically, you need to modify the 'keybinding.json' in VS Code:

> You can also open the keybindings.json file from the Command Palette (⇧⌘P) with the Preferences: Open Keyboard Shortcuts (JSON) command.
{: .prompt-info }

For instance, you can create a new hotkey with the following prompts. 

```bash
    {
        "key": "cmd+shift+B",
        "command": "editor.action.insertSnippet",
        "when": "editorLangId == latex && editorTextFocus",
        "args": {
            "snippet": "\\textbf{${TM_SELECTED_TEXT}$0}"
        }
    },
    {
        "key": "cmd+shift+I",
        "command": "editor.action.insertSnippet",
        "when": "editorLangId == latex && editorTextFocus", 
        "args": {
            "snippet": "\\textit{${TM_SELECTED_TEXT}$0}"
        }
    }
```

Then it will work. 

Same methods can be applied to Markdown, you can have a try, remember to modify the snippets.

P.S. If you are using Windows/Linux, remember to replace **cmd** with **ctrl**.


