<meta name="google-site-verification" content="MGrMbBi28Ut57MeqKI6srDSmlrprH0lug6rwNMIi0_A" />

# RemoteApp Tool

With Microsoft RemoteApp technology, you can seamlessly use an application that is running on another computer.

RemoteApp Tool is a utility that allows you to create/manage RemoteApps hosted on Windows (7, 8, 10, XP and Server) as well as generate RDP and MSI files for clients.

If you want your RemoteApps to appear in the Start Menu of your clients, or via a web interface, check out [RAWeb](https://github.com/kimmknight/raweb)!

If you have questions, comments or suggestions about RemoteApp Tool, please visit the [forum](https://groups.google.com/forum/embed/?place=forum/remoteapptool).

## Features

* Create and manage RemoteApps on Windows desktops and servers
* Generate RDP files
* Generate MSI installers (requires WiX Toolset)
* Use a Remote Desktop Gateway
* Set options such as session timeouts
* Select icons for your apps
* File type associations for deployed apps
* Sign RDP files
* Backup RemoteApps

## Requirements

* Microsoft .Net Framework 4
* [WiX Toolset](http://wixtoolset.org/) (If you want to create MSIs. Reboot after installing.)
* A **supported** edition of Windows XP, 7, 8, 10, or Server. See the [compatibility chart](https://github.com/kimmknight/remoteapptool/wiki/Windows-Compatibility).

**Note:** If you try to host RemoteApps on an incompatible edition of Windows (eg. Windows 10 Home), the tool will run but RemoteApps ***will not work***. The RDP client will appear to be connecting, then just disappear with no error shown.

## Download

**Latest:**

[RemoteApp Tool 6.0.0.0 Installer](https://github.com/kimmknight/remoteapptool/releases/download/v6.0.0.0/RemoteApp.Tool.6000.msi)

[RemoteApp Tool 6.0.0.0 Zip](https://github.com/kimmknight/remoteapptool/releases/download/v6.0.0.0/RemoteApp.Tool.6000.zip)

Please note: The latest installer no longer works on Windows XP, use the Zip instead.

**Previous:**

[RemoteApp Tool 5.3.0.0 Installer](http://www.kimknight.net/remoteapptool/RemoteApp%20Tool%205300.msi)

[RemoteApp Tool 5.3.0.0 Zip](http://www.kimknight.net/remoteapptool/remoteapptool5300.zip)

## User guide

[How to create a RemoteApp and use it on another computer](https://github.com/kimmknight/remoteapptool/wiki/Create-a-RemoteApp-and-use-it-on-another-computer)

## Screenshots

![Screenshot 1](https://raw.githubusercontent.com/wiki/kimmknight/remoteapptool/images/screenshots/ss1.png)

![Screenshot 2](https://raw.githubusercontent.com/wiki/kimmknight/remoteapptool/images/screenshots/ss2.png)

![Screenshot 3](https://raw.githubusercontent.com/wiki/kimmknight/remoteapptool/images/screenshots/ss3.png)

![Screenshot 4](https://raw.githubusercontent.com/wiki/kimmknight/remoteapptool/images/screenshots/ss4.png)

## Remote Desktop Plus
https://www.donkz.nl/overview-rdp-file-settings/

https://www.donkz.nl/companion-tools/#rdpprofile
gencrypt /p:P@sswordExample! /hash
password 51:b:01000000D08C9DDF0115D1118C7A00C04FC297EB010000008900A24423398E4EA9EE2994EDDAD7CB0000000002000000000
0106600000001000020000000B87BF10A058F690692221FA0AA4E05DF3D0961A852723EE19E689AAD70DB3DE3000000000E80000000020000
20000000C0359340A4331FBA676660F7ED98179A2B2EB6CD368B8A8AAC2B1EF16302E8DB3000000033A92D5F449479D1D4CC3E41C591ACF64
013C2A7D56A6AE968D28999AE017CE2BB3E794DCFFB2538C304C5304B35FEB540000000AFC52936246CC0D64A9D80EFEEA582DCD07EEA431C
22D85144368B19DCCF40D224E73BE69F46F890228396007EA3ED8327D28399CDA80A3D65467E95C78C88DA

http://technet.microsoft.com/en-us/library/ff393699(WS.10).aspx


