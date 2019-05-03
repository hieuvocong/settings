# Extensions
- Python
- Predawn Theme Kit
- Ayu
- Code Runner

# Format document
Use 'black'

# settings.json
```json
{
    "workbench.startupEditor": "newUntitledFile",
    "workbench.colorTheme": "Predawn",
    "workbench.iconTheme": "ayu",
    "workbench.statusBar.feedback.visible": false,
    "workbench.settings.editor": "json",
    "workbench.settings.openDefaultSettings": true,
    "window.zoomLevel": 1,
    "editor.mouseWheelZoom": true,
    "editor.minimap.enabled": false,
    "[plaintext]": {
        "editor.quickSuggestions": false
    },
    "editor.quickSuggestionsDelay": 100,
    "editor.fontFamily": "Source Code Pro",
    "editor.fontSize": 16,
    "editor.fontWeight": "500",
    "terminal.integrated.fontFamily": "Source Code Pro",
    "terminal.integrated.fontSize": 16,
    "terminal.integrated.fontWeight": "500",
    "debug.console.fontFamily": "Source Code Pro",
    "debug.console.fontSize": 16,
    "editor.formatOnSave": true,
    "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
    "python.pythonPath": "C:\\Users\\Cong-Hieu\\AppData\\Local\\Programs\\Python\\Python37\\python.exe",
    "python.linting.pylintPath": "C:\\Users\\Cong-Hieu\\AppData\\Roaming\\Python\\Python37\\Scripts\\pylint.exe",
    "python.linting.pylintArgs": [
        "--disable = F0401"
    ],
    "python.formatting.blackPath": "C:\\Users\\Cong-Hieu\\AppData\\Roaming\\Python\\Python37\\Scripts\\black.exe",
    "python.formatting.provider": "black",
    "code-runner.executorMap": {
        "python": "$pythonPath -u $fullFileName"
    },
    "code-runner.clearPreviousOutput": true,
    "code-runner.showExecutionMessage": false
}
```

# Fix context menu
Create a file with a ".reg" extension.
```
Windows Registry Editor Version 5.00

; Open files

[HKEY_CLASSES_ROOT\*\shell\Open with VS Code]
@="Edit with VS Code"
"Icon"="C:\\Users\\Cong-Hieu\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe,0"

[HKEY_CLASSES_ROOT\*\shell\Open with VS Code\command]
@="\"C:\\Users\\Cong-Hieu\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\" \"%1\""

; This will make it appear when you right click ON a folder
; The "Icon" line can be removed if you don't want the icon to appear

[HKEY_CLASSES_ROOT\Directory\shell\vscode]
@="Open Folder as VS Code Project"
"Icon"="\"C:\\Users\\Cong-Hieu\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\",0"

[HKEY_CLASSES_ROOT\Directory\shell\vscode\command]
@="\"C:\\Users\\Cong-Hieu\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\" \"%1\""

; This will make it appear when you right click INSIDE a folder
; The "Icon" line can be removed if you don't want the icon to appear

[HKEY_CLASSES_ROOT\Directory\Background\shell\vscode]
@="Open Folder as VS Code Project"
"Icon"="\"C:\\Users\\Cong-Hieu\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\",0"

[HKEY_CLASSES_ROOT\Directory\Background\shell\vscode\command]
@="\"C:\\Users\\Cong-Hieu\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe\" \"%V\""
```