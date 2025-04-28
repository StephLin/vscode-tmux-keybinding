# VSCode Tmux Keybinding

<img src="https://raw.githubusercontent.com/StephLin/vscode-tmux-keybinding/master/images/icon.png" height="128">

[[VS Code Marketplace](https://marketplace.visualstudio.com/items?itemName=stephlin.vscode-tmux-keybinding)] [[Open VSX Registry](https://open-vsx.org/extension/stephlin/vscode-tmux-keybinding)]

This is a simple extension for tmux behavior in the VS Code terminal. It provides keybindings similar to tmux, using either `Ctrl+B` (default) or `Ctrl+A` as a prefix.

## Configuration

You can configure which prefix key to use in your VS Code settings (`settings.json`):

```json
{
  // Enable keybindings that use Ctrl+B as a prefix (default: true)
  "tmuxKeybinding.enableCtrlBPrefix": true,

  // Enable keybindings that use Ctrl+A as a prefix (default: false)
  "tmuxKeybinding.enableCtrlAPrefix": false
}
```

## Keybinding

All keybindings are active only when the terminal has focus (`terminalFocus`).

### General Bindings

| Shortcut      | Command                                   | Description             |
| ------------- | ----------------------------------------- | ----------------------- |
| `ctrl+k`      | `workbench.action.terminal.clear`         | Clear terminal          |
| `shift+right` | `workbench.action.terminal.focusNext`     | Focus next terminal     |
| `shift+left`  | `workbench.action.terminal.focusPrevious` | Focus previous terminal |

### Prefix Bindings (`Ctrl+B` or `Ctrl+A`)

The following bindings work when the corresponding prefix (`tmuxKeybinding.enableCtrlBPrefix` or `tmuxKeybinding.enableCtrlAPrefix`) is enabled in settings. Replace `prefix` with `ctrl+b` or `ctrl+a`.

| Shortcut                | Command                                          | Description                      | Condition (if any)                          |
| ----------------------- | ------------------------------------------------ | -------------------------------- | ------------------------------------------- |
| `prefix c`              | `workbench.action.terminal.newInActiveWorkspace` | New terminal                     |                                             |
| `prefix 1` - `prefix 9` | `workbench.action.terminal.focusAtIndexN`        | Focus terminal by index          |                                             |
| `prefix shift+5`        | `workbench.action.terminal.split`                | Split terminal (horizontal)      | Panel at bottom                             |
| `prefix shift+'`        | `workbench.action.terminal.split`                | Split terminal (vertical)        | Panel not at bottom                         |
| `prefix alt+up`         | `workbench.action.terminal.resizePaneUp`         | Resize pane up                   |                                             |
| `prefix alt+down`       | `workbench.action.terminal.resizePaneDown`       | Resize pane down                 |                                             |
| `prefix alt+left`       | `workbench.action.terminal.resizePaneLeft`       | Resize pane left                 |                                             |
| `prefix alt+right`      | `workbench.action.terminal.resizePaneRight`      | Resize pane right                |                                             |
| `prefix ctrl+b`         | `workbench.action.toggleSidebarVisibility`       | Toggle sidebar visibility        | (Note: `ctrl+b` even if prefix is `ctrl+a`) |
| `prefix d`              | `workbench.action.terminal.toggleTerminal`       | Toggle terminal panel visibility |                                             |
| `prefix w`              | `workbench.action.quickOpenTerm`                 | Show terminal list               |                                             |
| `prefix z`              | `workbench.action.toggleMaximizedPanel`          | Toggle maximize terminal panel   |                                             |
| `prefix right`          | `workbench.action.terminal.focusNextPane`        | Focus next pane                  | Panel at bottom                             |
| `prefix left`           | `workbench.action.terminal.focusPreviousPane`    | Focus previous pane              | Panel at bottom                             |
| `prefix down`           | `workbench.action.terminal.focusNextPane`        | Focus next pane                  | Panel not at bottom                         |
| `prefix up`             | `workbench.action.terminal.focusPreviousPane`    | Focus previous pane              | Panel not at bottom                         |
| `prefix x`              | `workbench.action.terminal.kill`                 | Kill active terminal/pane        |                                             |
