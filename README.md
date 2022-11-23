MacOS-like keyboard layouts for Windows
=======================================

QWERTY Windows keyboard layouts that have dead keys and special characters
mapped much like the [MacOS dead keys].

- Allows finger reflexes to be transferable between both platforms
- Easily type common "special" characters like ° and μ as well as accented keys
  without having to deal with the terrible US International layout.
- Easily type the most common currency symbols.

Maclike dead keys for ANSI keyboards
------------------------------------

A layout for ANSI (US style) keyboards. Primarily targetting Dell
"International English" keyboards.

This layout is based on the English-UK keyboard layout but changed to match
the ANSI layout. All default acute accents of the UK/Irish keyboard  can still
be typed by double pressing the dead key, e.g AtlGr+u AtlGr+u wil result in ú.

### Main layer, to use hold AltGr or Alt+Ctrl

![AltGr layer](img/mac-ansiAltGr.jpg)

### Second layer, to use hold Shift+AltGr or Shift+Alt+Ctrl

![Shift-AltGr layer](img/mac-ansiShftAltGr.jpg)

### Differences vs the MacOS alt layout:

- More accent combinations are supported.
- Accents on AltGr+vowel characters as defined by the system Windows UK English
  layout.
- Cent sign is removed to allow for ₹ (Rupee) sign on AltGr+4.
- AltGr+`~` (AltGr+Shift+`) is an alternative tilde dead key.

Maclike dead keys for ISO keyboards
-----------------------------------

A layout for ISO (UK style) keyboards. Primarily targetting HP "UK English"
keyboards.

This layout is based on the English-UK keyboard layout. All default acute
accents can still be typed by double pressing the dead key, e.g AtlGr+u AtlGr+u
wil result in ú.

### Main layer, to use hold AltGr or Alt+Ctrl

![AltGr layer](img/mac-isoAltGr.jpg)

### Second layer, to use hold Shift+AltGr or Shift+Alt+Ctrl

![Shift-AltGr layer](img/mac-isoShftAltGr.jpg)

### Differences vs the MacOS alt layout:

- More accent combinations are supported.
- Accents on AltGr+vowel characters as defined by the system Windows UK English
  layout.
- Cent sign is moved from AltGr+4 to AtlGr+# to allow for € sign on AltGr+4.
- AltGr+~ (AltGr+Shift+#) is an alternative tilde dead key.

MacOS 10.15 dead keys for reference
-----------------------------------

![MacOS dead keys](img/macos.png)

Supported symbols
-----------------

These layouts currently supports:

- Most Latin grave accents;
- All Latin acute accents (Basic latin, Latin-1 Supplement, Latin Extended-A,
  Latin Extended-B and Latin Extended Additional unicode blocks);
- Most Latin diaeresis accents (Basic latin, Latin-1 Supplement, and Latin
  Extended-A);
- Most Latin tilde accents (Basic latin, Latin-1 Supplement, and Latin
  Extended-A);
- Special characters available on the MacOS alt layout.

Installation and usage
----------------------

- Download maclike-ansi.zip or maclike-iso.zip in the [latest version of the keyboard package installer][release].
- Run setup.exe and restart Windows.
- Set up the keyboard on Windows. E.g on Windows 10:
  - Navigate to settings > Time & Language > Language
      - Click on your system language > options and "Add a keyboard"
      Or
      - Click on "Choose an input method to always use as default" if you prefer
        to always use the same layout.

Modifying
---------

To modify this keyboard layout, install [Microsoft Keyboard Layout Creator] and
open the maclike-dead-keys-ansi.klc or aclike-dead-keys-iso.klc file. The
Keyboard Layout installer can be generated using Project > Build DLL and Setup
Package.

Note that the keyboard layout needs to be fully uninstalled for this to work.

Note on un/reinstallation
-------------------------

This keyboard package can be uninstalled like any MSI package, e.g through
Setting > Add or remove programs or by launching the installer again.

However, doing so may not remove certain registry entries on some verions of
Windows (e.g Windows 10), preventing the keyboard layout to be modified. On
Windows 11 this does not seem to be the case.

In order to fully uninstall this keyboard package on Windows 10, e.g to install
a new/adapted version, the register entry needs to be removed. This is typically
the last entry in:

```
Computer\HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts
```

But it's best to double check the "Layout Text" value before removal.

For more info see ["How do I remove a keyboard layout" on MSDN][remove-layout].

[MacOS dead keys]: https://support.apple.com/en-ie/guide/mac-help/mh27474/mac
[Microsoft Keyboard Layout Creator]: https://www.microsoft.com/en-us/download/details.aspx?id=102134
[release]: https://github.com/seppestas/maclike-windows-keyboard-layout/releases/latest
[remove-layout]: https://social.msdn.microsoft.com/Forums/ie/en-US/6e143a03-3fda-43fd-831b-2c3056d732b1/how-do-i-remove-a-keyboard-layout
