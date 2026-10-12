# Scoop bucket for LAN Wi-Fi Manager

[![Tests](https://github.com/bilal-nasr/scoop-bucket/actions/workflows/ci.yml/badge.svg)](https://github.com/bilal-nasr/scoop-bucket/actions/workflows/ci.yml) [![Excavator](https://github.com/bilal-nasr/scoop-bucket/actions/workflows/excavator.yml/badge.svg)](https://github.com/bilal-nasr/scoop-bucket/actions/workflows/excavator.yml)

[Scoop](https://scoop.sh) bucket for [LAN Wi-Fi Manager](https://github.com/bilal-nasr/lan-wifi-manager), a free Windows app that switches your traffic from LAN to Wi-Fi when the wired connection stops working or gets poor, and back when it recovers.

## Install

```pwsh
scoop bucket add bilal-nasr https://github.com/bilal-nasr/scoop-bucket
scoop install bilal-nasr/lan-wifi-manager
```

Then start it with `lanwifimanager`. It needs administrator rights to change the network priority, so Windows shows a UAC prompt when it opens. The app adds its own **LAN Wi-Fi Manager** Start menu shortcut the first time it runs.

The exe is not code-signed. Scoop checks its SHA-256 hash, which is the same as on the [release page](https://github.com/bilal-nasr/lan-wifi-manager/releases).

## Update

Quit the app from the tray, then:

```pwsh
scoop update lan-wifi-manager
```

Installed through Scoop, the app's own update check only tells you that a new version is out and copies this command.

## Uninstall

Quit the app from the tray first. Before uninstalling, turn off **Start with Windows** and **Show in the Start menu and Windows search** in the app's settings, because `scoop uninstall` does not remove the app's own start-at-login task or Start menu shortcut. Then:

```pwsh
scoop uninstall lan-wifi-manager
```

Settings and logs stay in `%AppData%\LanWifiManager`.

## Questions and bugs

Please use the app's [issues page](https://github.com/bilal-nasr/lan-wifi-manager/issues).
