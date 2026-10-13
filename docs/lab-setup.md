# Lab setup

## Confirmed decisions

- Use Windows as the host.
- Use Kali Linux in a virtual machine.
- Publish learning progress in a public GitHub repository.

## Details still to record

- Virtualization application and version.
- Kali version and tool versions.
- Adapter model, hardware revision, chipset, and driver.
- Whether Kali detects the adapter and supports monitor mode.
- Authorized test network, band/channel, and client device, using aliases in public notes.

## First checks in Kali

Run these read-only commands in the Kali terminal:

```bash
lsusb
iw dev
iw list
```

Record which USB device is the adapter, the wireless interface name, and whether `monitor` appears under supported interface modes. Do not assume the interface is named `wlan0`.

The VM's ordinary virtual network connection is not equivalent to direct access to a wireless radio. A compatible USB adapter passed through to Kali is the planned capture route. Monitor-mode availability depends on the hardware and driver; see the [capture setup reference](references.md).

## First exercise: offline analysis

Before live capture, choose a documented wireless example from Wireshark's sample captures. Keep downloaded captures outside version control and record the source, filename, and any redistribution terms in the lab entry.

1. Open the capture in Wireshark.
2. Inspect the frame encapsulation and available radio information.
3. Apply the display filter `eapol`.
4. Record relevant packet numbers, directions, and message numbers where available.
5. Explain what is observed and what cannot be concluded.

## Later exercise: live capture

Once the adapter is verified, document the exact monitor-mode and channel configuration for that device. Start a capture on the lab channel, manually reconnect a test client, and save the result privately. Review the capture before publishing any excerpts.

## Results

No setup commands or capture experiments have been run in Kali for this project yet.
