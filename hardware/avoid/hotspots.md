[🔗](./hotspots.md)

To summarize:

1) Dedicated Hotspot devices aren't good for privacy/security.
2) Use airplane mode + Wi-Fi with [GrapheneOS](https://grapheneos.org/)' default per-connection MAC randomization for better privacy.

Using a very niche hardware device to connect to the network such as a standalone hotspot device stands out. Those devices are also far less secure than simply using a Pixel with [GrapheneOS](https://grapheneos.org/).
![hotspots](https://github.com/randomwithnoname/security-advice/blob/main/hardware/avoid/hotspots.jpg)
They typically don't get proper updates and lack basic security measures.
For example, MiFi X PRO is essentially a low-end, poorly secured Qualcomm smartphone with an outdated SoC in a different form factor.

https://inseego.com/products/mobile-hotspot-routers/mifi-x-pro/#product-specifications

"FIPS 140-2 Certified" mean they stick to outdated cryptography from 2002. Not a positive.

Look at their listed security features.
![hotspots](https://pbs.twimg.com/media/GaG06TRXcAAKSu9?format=jpg&name=small)

If you really want to have cellular done from a separate device, a used Pixel with [GrapheneOS](https://grapheneos.org/) is a good option. If you want a fresh identity for the cellular network, there isn't really much alternative to using both a fresh device and SIM. Wi-Fi has a much more private design.

MAC randomization alone was not enough. Wi-Fi has had major privacy improvements on common devices like iPhones and Pixels in recent years to neuter other tracking based on sequence numbers, etc. GrapheneOS is aware of 1 remaining issue which has is reported/accepted as a vulnerability.

Also, bear in mind that carrying around a Wi-Fi access point (AP) is the opposite of private. An AP has a persistent MAC even if it's random upon creating the AP such as making a hotspot with a phone. Wi-Fi does not have MAC rotation like Bluetooth Low Energy privacy extensions.

GrapheneOS uses per-connection MAC randomization and per-connection DHCP as improvements over the standard Android Open Source Project. The MAC still remains the same while connected, and an AP isn't going to cycle until it's reset. Wi-Fi does not try to do what BLE privacy extensions do.

To clarify, an access point means a router such as Wi-Fi hotspot from a phone. If you enable Wi-Fi hotspot, it chooses a random MAC and uses it until it's disabled. Bluetooth LE tries to provide privacy for a paired device being carried around incl. MAC rotation. Wi-Fi does not.

Using a separate hotspot device WiFi allows your location to be tracked by more parties via MAC address or SSID, while not solving the original cell tower triangulation location tracking problem.

You still have to trust that airplane mode works in your phone regardless, so what exactly does this achieve beyond trusting a provably less secure device, and how does it improve privacy?
