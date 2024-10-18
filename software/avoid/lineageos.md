[🔗](./lineageos.md)

LineageOS is not a hardened OS. It greatly reduces security compared to AOSP via added attack surface, a weakened security model, and slow patches.

LineageOS usually takes around 4 to 6 months to release updates, which is 4 to 6 months during which users do not have current security patches since the latest releases are required for them. Pixels run the latest OS release, so updates for firmware, drivers, etc., are included. The same applies to any device receiving the yearly update.

Android 14 was released in October 2023. This was GrapheneOS's initial non-experimental public release based on it:

https://grapheneos.org/releases#2023100800

LineageOS released its initial Android 14 version in February 2024. Pixel users with LineageOS missed around half the patches during that delay.

For many devices, they don't even actually ship firmware and driver updates but rather leave the components that were included in the stock OS. The lack of shipping everything is a factor in why they don't provide any support for verified boot and related features.

It's not only LineageOS that experiences these kinds of delays. There are supposedly privacy- and security-focused projects with comparable delays to LineageOS, some of them around half the delay and others much longer. Some don't even do basic patching well, let alone hardening anything.

The Android security patches are far from perfect themselves, but shipping those properly is at least a good starting point. GrapheneOS ships the kernel patches much earlier and backports mainline module patches since often those receive important privacy and security fixes a month or two early.

LineageOS has network toggles that are leaky. The VPN features are misguided and anti-privacy.

Their tethering feature is incredibly leaky and is worse for privacy than a per-device tunnel. Android has per-profile VPN support as one of the major reasons for profiles to exist. They put effort into undoing that and pushing users to use a less private approach.

USB port control is based on the standard Android USB device admin toggle. They present it as disabling data, but it doesn't actually do that. It only disables high-level USB functionality, and they weakened it further in LineageOS with a major change.

They add a lot of attack surface and a few mostly incorrectly implemented privacy and security features. AOSP is a more private and secure OS without these changes.
