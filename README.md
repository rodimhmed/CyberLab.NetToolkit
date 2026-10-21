# CyberLab & NetToolkit — Security Operations Studio

A client-side cybersecurity learning workspace for network simulation, PCAP review, configuration auditing, topology modeling, and basic network utilities.

## Packet-flow simulator
- TCP/UDP ports are validated in the range 1–65535. ICMP does not require a port.
- Rule templates: Web default, DMZ web access, strict deny, and custom rules.
- Rules are validated with line-specific errors. First matching rule wins; unmatched traffic is denied.
- Unified educational rule format: `ACTION PROTOCOL SOURCE DESTINATION PORT`, for example `ALLOW TCP * * 443`. `*` and `ANY` are wildcard values.
- This is a browser-based educational simulator, **not Cisco Packet Tracer**. It does not open or export Cisco `.pkt` files and does not control live network equipment.

## Other features
- Local classic-PCAP parser (Ethernet + IPv4 summaries; PCAPNG not supported).
- Heuristic configuration review.
- Topology and threat-model canvas with SVG export and print/PDF.
- Troubleshooting challenges, IPv4/CIDR calculator, DNS-over-HTTPS, crypto utilities.
- Local project save/import/export and optional GitHub Gist publishing.
- Matrix background and responsive canvas sizing.

## Run
Open `index.html` in a modern browser or publish the project to GitHub Pages. DNS-over-HTTPS and GitHub Gist features require an internet connection.

## Validation performed
- JavaScript syntax check (`node --check`).
- HTML ID/reference consistency check (no duplicate IDs or missing `$()` targets found).
- Packet simulator unit smoke tests: HTTPS allowed, Telnet blocked, ICMP without a port, and malformed rule reporting.
- ZIP archive integrity check.

The app has not been fully exercised across all browsers or against live network equipment. Review all configuration advice before production use.
