# Wi-Fi Security Analyzer

A learning project exploring wireless frames, connection handshakes, and evidence-based security analysis with SEED Ubuntu Linux, Wireshark, and eventually Python.

## Current status

**Planning and lab preparation.** The learning documentation has been started. Wireless capture has not yet been verified, and the analyzer has not been implemented. This repository will document experiments, mistakes, findings, and the code developed along the way.

## Learning goals

- Understand 802.11 management, control, and data frames.
- Capture wireless traffic in an authorized lab and explain capture limitations.
- Identify EAPOL-Key messages in a WPA2 four-way handshake.
- Distinguish observed messages, retransmissions, and gaps in a capture.
- Build an offline analyzer that connects each finding to packet evidence.

## Planned lab

| Component | Status |
| --- | --- |
| Host operating system | Windows |
| Analysis environment | SEED Ubuntu Linux virtual machine |
| Virtualization application | VirtualBox (version to be recorded) |
| USB Wi-Fi adapter and chipset | To be confirmed |
| Monitor-mode support | Not verified |
| Test network and client | To be documented |
| Tools | Wireshark installed; TShark availability to be checked; Python planned |

## Explore the project

- [Lab setup](docs/lab-setup.md)
- [Learning journal](docs/learning-journal.md)
- [Reusable lab entry](docs/lab-entry-template.md)
- [Development roadmap](docs/roadmap.md)
- [Reference material](docs/references.md)

## Planned analyzer

The initial implementation will read saved `.pcap` or `.pcapng` files, use TShark to decode frames, and use Python to organize the results. Planned output includes a frame summary and a timeline of handshake messages for each access point/client pair.

Reports will distinguish observations from interpretations. A missing handshake message means it was not observed in the capture; that alone does not prove a failed connection. Four EAPOL packets alone do not prove a complete, coherent four-way handshake.

## Milestones

- [x] Define the project and start the learning documentation.
- [ ] Verify the SEED Ubuntu VM and capture hardware.
- [ ] Analyze a published sample capture.
- [ ] Capture a test device reconnecting to an authorized lab network.
- [ ] Explain a handshake using packet-level evidence.
- [ ] Implement and validate the offline analyzer.
- [ ] Publish an annotated example report.

## Capture handling

Experiments will use networks owned by the learner or explicitly authorized for testing. Raw captures, credentials, and local notes are excluded from version control by default. Only reviewed, sanitized examples should be published. Ignoring a file does not sanitize it or remove a previously committed copy.

## Learning approach

Each lab records a question, method, evidence, interpretation, limitations, and next steps. Planned work is marked as planned; completed experiments will include their actual observations.
