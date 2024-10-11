# [CalyxOS](https://github.com/randomwithnoname/security-advice/tree/main/avoid/calyxos.md)
CalyxOS is promoted as being privacy and security focused but it weakens both compared to the Android Open Source Project (AOSP). It often falls weeks or even months behind on standard privacy/security patches and introduces new vulnerabilities. They mislead their users about this.

They make inaccurate claims about which patches are shipped in each of their release notes and set an inaccurate Android security patch level field. They downplay the importance of shipping these patches. Their own changes largely reduce rather than improving privacy/security.

CalyxOS uses the [problematic microG](https://github.com/randomwithnoname/security-advice/blob/main/avoid/microg.md).
They have what they call a firewall app which is simply the leaky LineageOS network toggles moved out of the Settings app for marketing purposes. There's a dangerous panic feature taken from elsewhere with unreliable data deletion. The VPN features are misguided and anti-privacy.

VPN tethering feature from LineageOS is incredibly leaky and is worse for privacy than a per-device tunnel. Android has per-profile VPN support as one of the major reasons for profiles to exist. They put effort into undoing that and pushing users to use a less private approach.

USB port control from LineageOS is based on the standard Android USB device admin toggle. They present it as disabling data, but it doesn't actually do that. It only disables high level USB functionality, and they weakened it further in LineageOS/CalyxOS with a major change.

This kind of approach is endemic for both LineageOS and CalyxOS, which share a lot of the same developers. They add lots of attack surface and a few mostly incorrectly implemented privacy and security features. AOSP is a more private and secure OS without these changes.
