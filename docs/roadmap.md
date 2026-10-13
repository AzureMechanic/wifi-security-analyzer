# Development roadmap

## 1. Establish the lab

Record the VM, adapter, driver, and tool versions. Verify wireless visibility and monitor-mode support, or use a published sample capture to start.

Completion evidence: reproducible setup notes and an explanation of the available capture interface.

## 2. Inspect frames manually

Study management, control, and data frames. Inspect EAPOL-Key fields and explain a WPA2 four-way handshake using actual packet numbers.

Completion evidence: one lab entry with observations, interpretation, and capture limitations.

## 3. Build an offline command-line analyzer

Planned pipeline:

```text
Capture file -> TShark decoding -> Python analysis -> evidence-linked report
```

Start with input validation and frame summaries. Add handshake grouping by access point/client and exchange context, accounting for timing, direction, replay counters, nonces, and retransmissions. Treat incomplete or ambiguous captures explicitly.

Completion evidence: a repeatable command and a report checked against manual Wireshark inspection.

## 4. Validate and explain limitations

Use reviewed fixtures covering a complete exchange, missing messages, retries, multiple clients, and a file with no EAPOL frames. Include malformed input and missing-tool errors.

Completion evidence: documented expected outcomes and meaningful automated checks.

## 5. Publish a portfolio example

Publish a sanitized report and annotated screenshots. Explain what was learned, what the analyzer can establish, and what remains unsupported. Add installation and usage instructions once the implementation exists.
