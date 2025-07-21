# rofi-brbw

Yet another Rofi frontend for Bitwarden ([rbw](https://github.com/doy/rbw)).

![rofi-brbw](https://user-images.githubusercontent.com/32964025/213987598-95d60010-2c00-4c6a-96f7-85784b266e0f.png)

### Features

- Auto-type/copy {Username, Password, OTP, URL}
- Add/Remove items
- Modify an existing password
- Generate a new password
- Display fields/history of a selected item

### Dependencies

- [`rofi`](https://github.com/davatorium/rofi)
- [`rbw`](https://github.com/doy/rbw)
- `bash`, `coreutils`
- `sed`, `awk`
- `wl-clipboard`
- `xdg-utils`
- `wtype`
- `qrencode` *(for QR code generation)*
- `Nerd Font` or `Font Awesome` *(for icons)*

### Configuration

You can override default options by copying [`config.example`](config.example) file to `~/.config/rofi-brbw.conf`.

### Usage

Before running this script, you must configure `rbw`. Then you can run `rofi-brbw`.

If the database is locked, `rbw` will ask for the password using the pinentry dialog.

All available keybindings are listed below.

Keybinding                                       | Action
------------------------------------------------ | ------
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>u</kbd>  | Type Username
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>p</kbd>  | Type Password
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>t</kbd>  | Type OTP
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>l</kbd>  | Open URL
<kbd>Return</kbd>                                | Type Username <*tab*> Password
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>,</kbd>  | Copy Username
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>.</kbd>  | Copy Password
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>-</kbd>  | Copy OTP
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>m</kbd>  | Copy URL
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>q</kbd>  | Generate and display QR code
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>g</kbd>  | Generate and copy a new password
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>a</kbd>  | Add a new password to the database[^1]
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>e</kbd>  | Modify selected item's password[^1]
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>Del</kbd>| Remove selected entry with confirmation
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>v</kbd>  | View selected entry
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>n</kbd>  | View the password history for selected entry
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>c</kbd>  | Clear last used items
<kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>s</kbd>  | Sync Bitwarden database
<kbd>F1</kbd>                                    | Display key bindings

[^1]: These shortcuts requires you to configure `Editor` variable.

### Similar Projects

- [rofi-pass](https://github.com/carnager/rofi-pass) - Inspired me to write this script.
- [rofi-rbw](https://github.com/fdw/rofi-rbw) - rofi frontend for rbw written in python.

