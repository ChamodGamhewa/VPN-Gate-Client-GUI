# VPN Gate Client GUI

A simple Windows app for connecting to free public VPN servers from [VPN Gate](https://www.vpngate.net/EN/). Pick a server from the list and connect with one click.

![Icon](icon.ico)

## What you get

- A live **server list** with country, type, IP, port, protocol, speed, ping and score. Click any column to sort, or type in the search box to filter.
- **Server types** so you can see who runs a server:
  - **Academic** – official VPN Gate research servers (University of Tsukuba), shown in blue
  - **Volunteer** – personal computers run by individuals
  - **Other** – named third-party operators
- **One-click Connect / Disconnect** with live details: server, address, protocol, speed and ping, operator, your new public IP and a connection timer.
- **Automatic server list updates** on start and every 30 minutes (when not connected). The last list is saved, so the app still works offline.
- **Test all** – quickly checks which servers answer.
- **Windows notifications** when you connect, disconnect, lose the connection or a connection fails.
- **Log** panel with the connection output, and an **Info** window with version and author links.

## Installation

No installation or Python is needed.

1. Copy the whole folder to anywhere on your PC. Keep these files together:

   ```
   VPNGate.exe
   openvpn.exe
   libcrypto-3-x64.dll
   libssl-3-x64.dll
   libpkcs11-helper-1.dll
   vcruntime140.dll
   ```

2. Make sure a VPN network adapter is installed on your PC. If you have never used OpenVPN, install the free [OpenVPN Community](https://openvpn.net/community-downloads/) once to add it. The app shows a "no VPN network adapter" warning if it is missing.

3. Double-click **VPNGate.exe**.

## How to use

1. Start `VPNGate.exe` and click **Yes** on the Windows Administrator prompt. Administrator rights are required to create the VPN connection.
2. Choose a server. Fast ones have a high **Mbps** and low **Ping**. Use the filter buttons (All / Academic / Volunteer / Other) or the search box to narrow the list.
3. Click **Connect** (or double-click a row). The ring turns green when you're protected and your new public IP appears in the left panel.
4. Click **Disconnect** when you're finished. Closing the app also disconnects.

Toolbar buttons:

| Button | What it does |
| --- | --- |
| **Open** | Load a VPN Gate server list from a CSV file |
| **Fetch latest** | Download a fresh server list now |
| **Test all** | Check which servers are reachable |
| **Log** | Show or hide the connection log |
| **Info** | Version information and author links |
| **Check for updates** | Look for a newer version |

## Updates

The app checks for a new version on start and once a day. When one is found, a **required update** screen appears and the app cannot be used until you update. Click **Download update** to open the download page, replace `VPNGate.exe` with the new file, and start it again. **Quit** closes the app.

## Troubleshooting

| Problem | What to try |
| --- | --- |
| Connection fails or times out | Try another server. Many free servers are offline or blocked on your network. Use **Test all** first. |
| "No VPN network adapter" warning | Install OpenVPN Community once to add the adapter driver. |
| App does not start | Make sure all files listed above are in the same folder as `VPNGate.exe`. |
| Windows SmartScreen or antivirus warning | The app is not code-signed. Choose **More info → Run anyway** if you trust the file. |
| No notifications | Check that Windows notifications and Focus Assist are not blocking them. |

## Privacy and safety

- VPN Gate servers are run by volunteers. Operators may be able to see or log your traffic, so avoid signing in to sensitive accounts over them.
- The **Type** label is a best guess from the operator name VPN Gate publishes. It is not a guarantee of who runs a server or what they log.
- After you connect, the app asks `api.ipify.org` once to show your public IP. Server lists come from `vpngate.net`, and update checks go to GitHub.

## About

**VPN Gate Client GUI** · Version 1.0.1

- LinkedIn: <https://linkedin.com/in/chamod-gamhewa>
- GitHub: <https://github.com/ChamodGamhewa>
- Website: <http://chamodgamhewa.com/>
