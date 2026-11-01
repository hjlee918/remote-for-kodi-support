# Privacy Policy

**Remote for Kodi** (Stream Deck plugin), published by Artifex.
Effective date: October 31, 2026.

## Summary

The plugin does not collect, sell, or share personal data. It does not send anything to us or to any server on the internet. Everything it needs stays on your computer and travels only between your computer and Kodi on your local network.

## What the plugin stores, and where

The plugin saves the following in Stream Deck's settings on your computer:

- Each Kodi device you set up: its name, IP address and ports, the identifier Kodi announces on the network, its network (MAC) address, and its Kodi and system versions.
- The username and password you entered for Kodi's web server. They are stored on your computer only and sent only to that Kodi device.
- What you chose for each key or dial, for example "Volume up" or a favourite to open, and for favourite and add-on keys their name and thumbnail, so the key looks right while Kodi is off.

This information never leaves your computer except as described below. To delete it, click **Forget** next to a device in any key's settings, or uninstall the plugin.

## Network use

The plugin communicates only with Kodi devices on your local network:

- **Search** sends a standard discovery message (Zeroconf / mDNS) on your local network to find Kodi, or checks the IP address you enter.
- **Test connection**, every key press and every dial turn send commands directly to Kodi. While a key or dial is on your Stream Deck, the plugin keeps a connection to Kodi open so the key can show Kodi's state (for example its volume, or what's playing).
- Artwork and thumbnails are downloaded from Kodi itself, never from the internet.
- **Power on** sends a Wake-on-LAN packet on your local network.

The plugin makes no connections to the internet. It contains no analytics, tracking, or advertising.

## Logs

Stream Deck keeps a plugin log on your computer to help diagnose problems:

- macOS: `~/Library/Application Support/com.elgato.StreamDeck/Plugins/com.johnlee.kodiremote.sdPlugin/logs/`
- Windows: `%APPDATA%\Elgato\StreamDeck\Plugins\com.johnlee.kodiremote.sdPlugin\logs\`

The log can include your Kodi device's name and IP address and messages about commands that failed. It does not include the password or what you watch. The log stays on your computer unless you choose to share it.

## Support requests

If you open an issue in this repository, the issue and anything you attach to it (such as a log) are **public on GitHub** and subject to [GitHub's Privacy Statement](https://docs.github.com/site-policy/privacy-policies/github-general-privacy-statement). Remove anything you don't want to share before posting.

## Purchases

Purchases on the Elgato Marketplace are handled by Elgato (Corsair) and its payment processor, Stripe. We do not receive your payment details. Elgato's privacy policy and [Stripe's Privacy Policy](https://stripe.com/privacy) describe how they handle your data.

## Changes

If this policy changes, the updated version will be posted here with a new effective date.

## Contact

Questions about this policy: [open an issue](https://github.com/hjlee918/remote-for-kodi-support/issues).
