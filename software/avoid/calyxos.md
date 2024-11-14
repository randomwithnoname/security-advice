[🔗](./calyxos.md)

CalyxOS is still based on Android 14 QPR3 without the full October security patches or the already released November security patches.
As of November 14 2024, CalyxOS is promoted as being privacy and security focused, but it weakens both compared to the Android Open Source Project (AOSP). It often falls weeks or even months behind on standard privacy and security patches and introduces new vulnerabilities. They mislead their users about this.

They support insecure devices and mislead users about the security of them, including end-of-life Pixel devices. No OS can make a device not recieving OEM support secure. Period.

They make inaccurate claims about which patches are shipped in each of their release notes and set an inaccurate Android security patch level field. They downplay the importance of shipping these patches. Their own changes largely reduce rather than improve privacy and security.

CalyxOS uses the [problematic microG](./microg.md).

They have what they call a firewall app, which is simply the leaky [LineageOS](./lineageos.md) network toggles moved out of the Settings app for marketing purposes. There's a dangerous panic feature taken from elsewhere with unreliable data deletion. The VPN features are misguided and anti-privacy.

The VPN tethering feature from LineageOS is incredibly leaky and is worse for privacy than a per-device tunnel. Android has per-profile VPN support as one of the major reasons for profiles to exist. They put effort into undoing that and pushing users to use a less private approach.

The Calyx Institute also gives away as a perk of being a member of their "charity" (sells) [insecure mobile hotspot devices](/hardware/avoid/hotspots.md) to be used with resold T-Mobile service, and they're supposedly trying to improve user privacy and security...

USB port control from LineageOS is based on the standard Android USB device admin toggle. They present it as disabling data, but it doesn't actually do that. It only disables high-level USB functionality, and they weakened it further in LineageOS/CalyxOS with a major change.

This kind of approach is endemic to both LineageOS and CalyxOS, which share many of the same developers. They add a lot of attack surface and a few mostly incorrectly implemented privacy and security features. AOSP is a more private and secure OS without these changes.
