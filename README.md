# Open with Cursor (Registry)

> Add Cursor to the Windows context menu with per-user registry files.

<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-f59e0b?style=flat" alt="License: MIT"></a>
  <img src="https://img.shields.io/badge/Platform-Windows-0078d4?style=flat" alt="Platform: Windows">
  <img src="https://img.shields.io/badge/Registry-Per%20user-5391fe?style=flat" alt="Registry: Per user">
</p>

<p>
  <a href="#usage">Get started</a> · <a href="LICENSE">License</a> · <a href="README_zh-CN.md">中文说明</a>
</p>

This project adds Cursor editor options to the Windows context menu for files, folders, and folder backgrounds by modifying the Windows registry.

## Features

- Adds "Open with Cursor" option to the context menu for files, folders, and folder backgrounds
- Adds "通过 Cursor 打开" option for Chinese language users
- No administrator privileges required
- User-specific installation (affects only current user)
- Uses current-user registry entries; availability on managed devices depends on local policies

## Usage

### Quick Installation (Recommended)

Requires Windows with Cursor already installed. Download or clone this repository, then choose one menu language:

1. **Modify Configuration**: Open the `.reg` file you want to use and replace all `<YourUsername>` with your Windows profile folder name. If Cursor uses a custom installation location, replace every executable path with its actual path, preserving the doubled backslashes in the `.reg` file.
2. **Install one variant**:
   - **English**: Double-click the modified `install-open-with-cursor.reg`
   - **Chinese**: Double-click the modified `install-open-with-cursor-zh.reg` (UTF-16 LE encoded)
3. Click "Yes" when Windows asks for confirmation
4. Restart File Explorer or log out and back in

### Uninstallation

1. Double-click `uninstall-open-with-cursor.reg`
2. Click "Yes" when Windows asks for confirmation
3. Restart File Explorer or log out and back in

**Note:** The registry files use `HKEY_CURRENT_USER` instead of `HKEY_CLASSES_ROOT`, making the installation user-specific and eliminating the need for administrator privileges.

## Files

- `install-open-with-cursor.reg` - Install script (English)
- `install-open-with-cursor-zh.reg` - Install script (Chinese, UTF-16 LE encoded)
- `uninstall-open-with-cursor.reg` - Uninstall script (works for both languages)

## Manual Installation Steps

If you prefer to manually edit the registry:
- For detailed manual installation steps, please refer to [README_en.md](README_en.md).
- For detailed manual installation steps (in Chinese), please refer to [README_zh-CN.md](README_zh-CN.md).


## Related Projects

- [Open-with-Cursor](https://github.com/yuzhounh/Open-with-Cursor) - The Python/EXE alternative for Cursor, which writes to `HKEY_CLASSES_ROOT` and requests administrator privileges.

- [Open-with-Antigravity](https://github.com/yuzhounh/Open-with-Antigravity) - A separate context-menu tool for the Antigravity editor, with multiple per-user installation methods.

- [Open with Cursor in Context Menu](https://github.com/Puliczek/open-with-cursor-context-menu) - A similar project that uses PowerShell scripts to achieve similar functionality.

- [cursor_ext_open-with-cursor-context-menu](https://github.com/eatcosmos/cursor_ext_open-with-cursor-context-menu) - A fork of the above project that adds a batch file for easy installation with a double-click.

- [Cursor Context Menu Installer](https://github.com/hexcreator/open-with-cursor) - A similar project that uses C++ scripts to achieve similar functionality.

## License

This project is licensed under the [MIT License](LICENSE).

## Acknowledgments

Special thanks to [Ryan Johnson](https://github.com/AMDphreak) for his original contribution. This project is entirely based on his work. I only replaced the relative paths with absolute paths and conducted feasibility testing.

## Contact

Jing Wang - wangjing@xynu.edu.cn

Project Link: https://github.com/yuzhounh/Open-with-Cursor-by-reg
