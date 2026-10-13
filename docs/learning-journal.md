# Learning journal

## 2026-10-13 — Project definition

### Question

How can I learn to dissect Wi-Fi frames and turn that knowledge into a useful analyzer?

### Decisions

- Use a SEED Ubuntu Linux VM in VirtualBox on Windows as the lab environment.
- Start with Wireshark inspection before automating analysis.
- Document progress publicly on GitHub.
- Build an offline analyzer using TShark and Python after the first capture exercises.

### Evidence and current status

These are planning decisions. No lab capture, handshake identification, or analyzer execution has been completed yet. The learner confirmed VirtualBox and SEED Ubuntu Linux, with Wireshark installed. Exact versions and the adapter model still need to be recorded.

### Next experiment

Verify adapter visibility in SEED Ubuntu, or start with a published sample capture if capture hardware is not available. Use the [lab entry template](lab-entry-template.md) to record actual findings.

## 2026-10-13 — First working network capture

### Objective

Confirm that Wireshark can capture browser traffic inside the SEED Ubuntu VM.

### Problem and resolution

Initially, no packets appeared while using Firefox. An active filter was present; clearing it resolved the issue. The exact filter was not recorded, and a software bug has not been established.

### Evidence

Wireshark captured traffic on `enp0s3`. The first successful screenshot showed 474 captured packets and 474 displayed packets, with TCP and TLS traffic. A later screenshot showed the learner inspecting Ethernet, IPv4, and TCP packet details.

### Lesson learned

Start the first capture with both capture and display filters empty. Confirm traffic is visible, then apply filters deliberately. A display filter hides packets from view; a capture filter excludes packets from collection.

### Limitations and next step

This was ordinary VM network traffic, not raw 802.11 frames or a Wi-Fi four-way handshake. Continue inspecting protocol layers, then use a published wireless capture for the handshake exercise.
