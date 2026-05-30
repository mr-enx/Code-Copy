# Code Copy

**Code Copy** is a VS Code extension for quickly selecting files from your workspace and copying their contents or paths to the clipboard.

It provides an explorer-like sidebar UI with search, file selection, include/exclude filters, and project-level settings.

---

## Features

### File Selection

- Explorer-like file tree in the sidebar
- Select individual files with checkboxes
- Search files and folders
- Select all currently visible files with a toggle button
- Expand or collapse folders
- Refresh the file list from the view title bar

### Copy Actions

- Copy selected file contents to the clipboard
- Copy selected file paths to the clipboard
- Automatically respects active filters and selected files

### Filtering

Code Copy supports two filter modes:

- **Exclude**  
  Ignore files that match the provided extensions or patterns.

- **Only include**  
  Copy only files that match the provided extensions or patterns.

### Settings

A dedicated settings page is available from the view title bar.

Settings include:

- Title
- Filter mode
- Exclude patterns
- Only include patterns

Settings are saved locally in your workspace:
```txt
.vscode/code-copy.json

---

## Sidebar UI

The Code Copy sidebar includes:

| Control | Description |
|---|---|
| Refresh icon | Reloads the workspace file list |
| Settings icon | Opens the settings page |
| Search input | Filters visible files and folders |
| Select Visible | Toggles selection of currently visible files |
| Expand All | Expands or collapses all folders |
| Copy Content | Copies selected file contents |
| Copy Paths | Copies selected file paths |

---

## Usage

### 1. Open Code Copy

Open the **Code Copy** view from the VS Code Activity Bar.

### 2. Select Files

Use the file tree to select the files you want to copy.

You can also use search and then click **Select Visible** to select only the filtered results.

### 3. Copy Content or Paths

Click one of the available actions:

- **Copy Content**
- **Copy Paths**

The result will be copied directly to your clipboard.

---

## Filter Examples

### Exclude mode

Use this mode when you want to ignore certain file types.

Example:

txt
.log
.tmp
.map

Files with these extensions will be excluded.

### Only include mode

Use this mode when you only want specific file types.

Example:

txt
.ts
.tsx
.json
.md

Only files with these extensions will be included.

---

## Configuration File

Code Copy stores project settings in:

txt
.vscode/code-copy.json

Example configuration:

json
{
  "title": "Project Source Files",
  "mode": "ignore",
  "exclude": ".log\n.tmp\n.map",
  "onlyInclude": ".ts\n.tsx\n.json",
  "selectedFiles": [
"src/extension.ts",
"package.json",
"README.md"
  ]
}

---

## Build & Run

### Install dependencies

bash
npm install

### Compile the extension

bash
npm run compile

This compiles the TypeScript source from `src/` into the `out/` folder.

### Run in development

Press `F5` in VS Code to launch the **Extension Development Host** with the extension loaded.

---

## Packaging

### Install VSCE

bash
npm install -g @vscode/vsce

### Create the VSIX package

bash
vsce package --allow-missing-repository

The generated `.vsix` file can be installed manually or published to the VS Code Marketplace.

---

## Install Locally

bash
code --install-extension code-copy-0.0.1.vsix

---

## License

MIT © [genius-programmer.com](https://genius-programmer.com)
