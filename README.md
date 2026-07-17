# Lab Simulations

A small collection of self-contained, browser-based labs for learning the basics
of the Linux command line and network security tooling. Each lab is a single HTML
file with no build step, no dependencies to install, and no real systems involved —
everything is simulated in JavaScript, so you can experiment safely.

## The Labs

| File | What it teaches |
| --- | --- |
| [`linux-terminal-beginners.html`](linux-terminal-beginners.html) | A simulated Linux shell with a mock filesystem. Practice `ls`, `cd`, `pwd`, `cat`, `echo`, `mkdir`, `touch`, `rm`, `rmdir`, and more, plus a reference table of common shell operators (`&`, `&&`, `>`, `>>`). |
| [`wireshark-beginners-interactive-lab.html`](wireshark-beginners-interactive-lab.html) | A guided Wireshark simulator with a pre-recorded packet capture. Learn to start/stop a capture and write display filters (`http`, `tls`, `ip.addr == ...`, combined filters). |
| [`tcpdump-lab-simulator.html`](tcpdump-lab-simulator.html) | A command-driven `tcpdump` simulator. Run live captures, filter for TCP, write and read `.pcap` files (with a simulated TCP three-way handshake), and try `nmap`/`wireshark` follow-ups. |
| [`pentest-beginners-interactive-lab.html`](pentest-beginners-interactive-lab.html) | A step-by-step guided penetration-test walkthrough against a simulated target: recon with `nmap`, vulnerability research with `searchsploit`, exploitation with Metasploit, and writing up a report. |

## Running the Labs

No server or installation is required. Either:

- **Open directly:** double-click any `.html` file, or drag it into your browser.
- **Serve locally** (optional, avoids some browser file-access quirks):

  ```bash
  # From the repository root
  python3 -m http.server 8000
  # then visit http://localhost:8000 and pick a lab
  ```

An internet connection is needed the first time you open a lab, because styling is
loaded from the Tailwind CSS CDN.

## How to Use Them

- **Linux terminal:** type `help` to list the available commands, then explore the
  mock filesystem. Command history works with the up/down arrow keys, and `Tab`
  offers basic name completion.
- **Wireshark lab:** follow the numbered steps in the left sidebar. Each step
  unlocks the next once you complete its task (starting a capture, applying a
  filter, and so on).
- **tcpdump simulator:** type `help` to see the supported commands. Use the
  **STOP CAPTURE** button or type `stop` to end a live capture.
- **Pentest lab:** each step tells you exactly which command to type. Type it into
  the terminal to reveal the simulated output and unlock the **Next Step** button.
  `help` and `clear` are available at any point.

## A Note on Safety and Scope

These labs are **simulations built for education**. No real network traffic is
captured, no real hosts are scanned, and no real exploits are run — every command
returns hard-coded or randomly generated sample output. The penetration-testing
lab in particular is meant to teach the *methodology* (recon → research →
exploitation → reporting) in a safe sandbox. Only ever run real security tools
against systems you own or have explicit written permission to test.

## Contributing

The labs are intentionally dependency-free single files, which makes them easy to
tweak: open a file, edit the embedded `<script>`, and reload the page to see your
change. Ideas for improvements — more commands, additional lab steps, clearer
explanations — are welcome.
