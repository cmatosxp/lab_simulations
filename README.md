# Interactive Cybersecurity Lab Simulations

Safe, browser-based practice labs for Linux, packet analysis, packet capture, and an authorized penetration-testing workflow. Every command and packet stays inside the page: the labs do not scan hosts, capture network traffic, or run real exploits.

## Launch a Lab

| Level | Live simulation | What you will practice | Source |
| --- | --- | --- | --- |
| Beginner | [Linux Foundations Lab](https://cmatosxp.github.io/lab_simulations/linux-terminal-beginners.html) | Navigate a mock filesystem, manage files and directories, search text, chain commands, pipe output, and use redirection across eight missions. | [`linux-terminal-beginners.html`](linux-terminal-beginners.html) |
| Intermediate | [Advanced Linux Terminal](https://cmatosxp.github.io/lab_simulations/linux-terminal-advanced.html) | Use 30+ simulated commands, manual pages, globbing, variables, pipes, redirection, exit status, conditional lists, permissions, and an 11-mission checklist. | [`linux-terminal-advanced.html`](linux-terminal-advanced.html) |
| Beginner | [Wireshark Analysis Lab](https://cmatosxp.github.io/lab_simulations/wireshark-beginners-interactive-lab.html) | Work a guided packet-investigation case, select evidence frames, inspect protocol details and bytes, and build Wireshark display filters. | [`wireshark-beginners-interactive-lab.html`](wireshark-beginners-interactive-lab.html) |
| Intermediate | [tcpdump Capture Lab](https://cmatosxp.github.io/lab_simulations/tcpdump-lab-simulator.html) | Inspect interfaces, run bounded captures, apply BPF capture filters, write/read an in-memory PCAP, and isolate TCP SYN packets across seven objectives. | [`tcpdump-lab-simulator.html`](tcpdump-lab-simulator.html) |
| Beginner | [Authorized Pentest Lab](https://cmatosxp.github.io/lab_simulations/pentest-beginners-interactive-lab.html) | Follow scope, discover and enumerate a training host, research a version-specific exposure, validate impact, collect evidence, clean up, and write a finding. | [`pentest-beginners-interactive-lab.html`](pentest-beginners-interactive-lab.html) |

## Recommended Learning Path

1. Start with **Linux Foundations** and complete all eight missions.
2. Move to the **Advanced Linux Terminal** for pipelines, permissions, search tools, conditional execution, and exit status.
3. Use the **Wireshark Analysis Lab** to learn display filters and packet inspection.
4. Use the **tcpdump Capture Lab** to learn capture filters and PCAP workflows from the command line.
5. Finish with the **Authorized Pentest Lab**, which combines scope control, methodology, evidence, cleanup, and reporting.

## Using the Labs

- Follow the mission or objective panel; it updates only after the required action succeeds.
- Type `help` in a terminal lab to see its supported command set.
- Use Up/Down for command history. Linux labs also support Tab completion; terminal labs support Ctrl+L to clear.
- Use each lab's reset control to restore its original state. Supported labs save progress in browser storage between reloads.
- Packet and security data are deterministic training scenarios, so findings are reproducible.

## Run Locally

There is no build step. Clone or download the repository, then either open an HTML file directly or serve the directory:

```bash
python3 -m http.server 8000
```

Open `http://localhost:8000/` and select a file. The Linux, Wireshark, and tcpdump labs load Tailwind CSS from its CDN for styling, so they need internet access for their full appearance. The pentest lab is fully self-contained.

## Safety and Scope

These are closed educational simulations. They generate no real packets and make no tool-driven network requests. Only use real administration, capture, scanning, or exploitation tools on systems you own or have explicit written authorization to test.

## Contributing

Each simulation is a single HTML file with embedded JavaScript. Keep command behavior, interface guidance, and README examples aligned; test both successful and failing paths before proposing a change.
