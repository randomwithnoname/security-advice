[🔗](./librem-5.md)

The Librem 5 is a highly insecure device without basic firmware security updates and hardware/software security features. It rolls back privacy and security by a decade. 

The hardware kill switches don't serve much purpose in general, but especially in the way the [Librem 5 implemented them](https://madaidans-insecurities.github.io/linux-phones.html#hardware-kill-switches).

Hardware kill switches are a last resort if your device gets compromised by an attacker. They still obtain all your data including your photos, videos, documents, passwords, login session, keys, etc. You only stop them using certain hardware while they're turned off.

Regardless, kill switches do not make up for the device having massive security flaws or insecure software.

A properly implemented audio recording kill switch prevents an attacker compromising the device from doing that while it's turned off. They can of course still record all your calls, get audio during video recording or any other time you leave it enabled. It's a last resort.

When the device has been compromised by an attacker with persistent full control over it and access to your data, accounts, keys, etc. you have far more problems than them recording audio with it. It addresses a very narrow part of what a secure device should be protecting from.

The Librem 5 does not have mostly open firmware. The hardware and firmware is nearly entirely closed source, including the whole CPU, GPU, SSD, memory, Wi-Fi, cellular, etc. The amount of the hardware/firmware that's open source is far under 1%. Boot chain is a tiny part of this. Laptops and desktops don't generally have any significant open source firmware or hardware. It's not something specific to smartphones or tablets. The idea that a cellular radio is uniquely closed source is wrong. It's the same as Wi-Fi, Bluetooth, NFC, GPU, CPU, etc. Similarly, the idea that a cellular radio has control over the device is completely wrong for modern smartphones. Purism has heavily participated in spreading this misconception. Mainstream phones like the iPhone have better isolated cellular than the Librem 5 or Pinephone. Isolation approach used for components like cellular radios in a modern smartphone is significantly lower attack surface than the attack surface exposed to any USB device. The idea cellular radio has privileged access and control of the device is simply wrong for modern phones. There are efforts to build open hardware/firmware laptops and desktops. The main one is the Talos II, which has largely open hardware/firmware for the motherboard. However, it does have closed source components and the CPUs are entirely closed hardware in practice, not open ones.
