# Remote for Kodi

Support page for **Remote for Kodi**, a Stream Deck plugin that controls Kodi® on any device (CoreELEC, LibreELEC, Nvidia Shield, Fire TV, Android boxes and PCs): remote buttons, playback with the artwork of what's playing, volume, library sections, favourites and add-ons, power, and Stream Deck + dials. Get it on the [Elgato Marketplace](https://marketplace.elgato.com/).

## Get help

- **Found a bug?** [Open a bug report](../../issues/new?template=bug_report.yml).
- **Have an idea?** [Suggest a feature](../../issues/new?template=feature_request.yml).

Please search [existing issues](../../issues) first.

## Requirements

- Windows 10 or later, or macOS 12 or later.
- Stream Deck 7.1 or later.
- Kodi 19 or later, on a device on the same network as the computer.

## Setup

1. **In Kodi**, open **Settings → Services → Control** and turn on:
   - **Allow remote control via HTTP**. Set a **username** and **password** on the same screen. The port stays 8080.
   - **Allow remote control from applications on other systems**.
2. Drag any **Remote for Kodi** action onto a key, for example **Remote Button**.
3. In its settings, click **Search** and choose your Kodi. If nothing is found, type Kodi's IP address in **Address**. The address is in Kodi under **Settings → System information → Network**.
4. Enter the **Username** and **Password** you set in Kodi, and click **Test connection**. The settings then show what works:
   - **Connected**: the keys can control Kodi.
   - **Username and password work**: the keys can also show artwork and thumbnails.
5. Choose what the key does. Add more keys for other actions; they all share the setup.

**More than one Kodi?** Click **Add Kodi** in any key's settings and set it up the same way. Each key or dial then has a **Control** menu for choosing its device; the first one set up is the default. To change a password, click **Change** next to the device.

## Turning the device on and off

The **Power** action can sleep, shut down, reboot or hibernate the device, or quit Kodi; the key tells you if the device can't do what you chose. **Shut down**, **Reboot** and **Power on / off** ask for a second press, so a stray press doesn't turn anything off (you can turn that off in the key's settings).

**Power on** uses Wake-on-LAN:

- **CoreELEC and LibreELEC boxes:** connect the box **by cable** and turn on Wake-on-LAN in the device. On CoreELEC it's in the **CoreELEC** settings. Some boxes can only be woken after Kodi shut them down, not after the power was unplugged. Waking over Wi-Fi doesn't work.
- **Nvidia Shield, Fire TV and other Android devices:** Kodi is an app there. It can't turn the device off or on; use **Quit Kodi** instead.
- **PCs:** turn on Wake-on-LAN in the PC's BIOS or network adapter settings, and connect it by cable.

The plugin learns the device's network (MAC) address from Kodi while it's connected, so set the device up while it's on.

## The actions

| Action | What it does |
|---|---|
| **Remote Button** | Any button of a Kodi remote: arrows, OK, Back, Home, context menu, Info, the player menu, subtitles, audio track, zoom, chapters, Live TV channels and color buttons, numbers and more. Can also type into Kodi's keyboard, show a message, update the library, or run any Kodi action. Optional **Hold** and **Double press** commands. |
| **Playback** | Play / pause, stop, next, previous, skip back or forward, rewind, fast forward, repeat, shuffle, subtitles and the audio track. Play / Pause shows the artwork of what's playing with a progress bar. |
| **Volume** | Volume up or down (hold to repeat), mute, or a set level. The key shows Kodi's volume. |
| **Library** | Opens Movies, TV Shows, Music, new episodes, In Progress, Live TV, the TV guide, Add-ons, Favourites, Settings and more. The key shows a bar while that part of Kodi is on screen. |
| **Favourites & Add-ons** | Opens one of your Kodi favourites, or a video, music, picture or program add-on, with its thumbnail on the key. |
| **Power** | Power on (Wake-on-LAN), sleep, shut down, reboot, hibernate, or quit Kodi. A green dot shows while Kodi is on. |
| **Kodi Dial** (Stream Deck +) | Volume, seek through what's playing (with its artwork and position on the touch strip), navigate menus, or scroll lists. |

## Troubleshooting

- **Search finds nothing:** make sure Kodi is running and on the same network as the computer, then type its IP address and click **Test connection**. Some routers and mesh Wi-Fi systems block automatic discovery.
- **"Kodi doesn't answer on port 9090":** turn on **Allow remote control from applications on other systems** in Kodi (Settings → Services → Control).
- **"Kodi refused the username or password":** check them in Kodi under Settings → Services → Control, then click **Change** next to the device and test again.
- **"Kodi's web server doesn't answer":** turn on **Allow remote control via HTTP**. The keys still work without it, but can't show artwork or thumbnails.
- **Keys say "Kodi is off" while it's on:** the device's IP address may have changed. The plugin looks for it again on its own; if that doesn't work, reserve a fixed IP address for the device in your router, then click **Change** and enter the new address.
- **No artwork on Play / Pause:** some items have none, and artwork needs the web server (see above).
- **The volume keys don't change the sound:** with audio passed through to an amplifier or soundbar (passthrough), Kodi's volume doesn't apply. Use the amplifier's volume.
- **Power on doesn't work:** see *Turning the device on and off*.
- **Windows asks whether to allow network access:** choose **Allow** so the plugin can find and control Kodi on your local network.

When reporting a bug, attach the latest log from:

- **macOS:** `~/Library/Application Support/com.elgato.StreamDeck/Plugins/com.johnlee.kodiremote.sdPlugin/logs/`
- **Windows:** `%APPDATA%\Elgato\StreamDeck\Plugins\com.johnlee.kodiremote.sdPlugin\logs\`

## Privacy

The plugin collects no personal data and connects only to Kodi on your local network. See the [Privacy Policy](PRIVACY.md).

## Open-source software

The plugin includes open-source software; see `THIRD_PARTY_NOTICES.txt` inside the plugin.

---

Kodi is a registered trademark of the XBMC Foundation. This plugin is not affiliated with, sponsored by, or endorsed by the XBMC Foundation. CoreELEC, LibreELEC, Nvidia Shield and Fire TV are trademarks of their respective owners.
