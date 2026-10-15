![A Great exploit user can run an masterpiece, but a masterpiece can build the exploit itself](./banner.svg?v=2)

<p align="center">
  <a href="https://pushpenderrathore.github.io/">Portfolio</a> ·
  <a href="https://pushpenderrathore.github.io/gsoc.html">GSoC 2026</a> ·
  <a href="https://www.linkedin.com/in/pushpender-singh-rathore-72466a260/">LinkedIn</a> ·
  <a href="mailto:enp7s0d@gmail.com">Email</a> ·
  <a href="https://pushpenderrathore.github.io/prs.html">Open-source PRs</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/GSoC%202026-Metasploit%20%C2%B7%20Rapid7-9FEF00?style=for-the-badge&logo=google&logoColor=0b0f14&labelColor=0b0f14"/>
  <img src="https://img.shields.io/badge/MSF%20PRs%20merged-12-9FEF00?style=for-the-badge&logo=metasploit&logoColor=white&labelColor=0b0f14"/>
  <img src="https://img.shields.io/badge/ruby__smb%20merged-1-9FEF00?style=for-the-badge&logo=ruby&logoColor=white&labelColor=0b0f14"/>
  <img src="https://img.shields.io/badge/Rapid7%20blog%20features-8-00D4FF?style=for-the-badge&logoColor=white&labelColor=0b0f14"/>
  <img src="https://img.shields.io/badge/CVE-2026--20929-FF4D4F?style=for-the-badge&logoColor=white&labelColor=0b0f14"/>
</p>

---

Hi. My name is Pushpender Singh Rathore, and I am an offensive security engineer and
open-source contributor. I build the tooling and framework code that red teams and
researchers actually run, and I ship it in public where anyone can read it, break it,
and use it.

I care about one thing above the rest: making offensive security legible. A proof of
concept that no one else can reproduce, read, or trust is a liability, not a result. So I
spend most of my time on the parts that rarely get attention: the traces, the presenters,
the specs, and the clean module code that turn a fragile one-off into something an
operator can depend on. That is the loop in the banner above. Recon, develop, exploit,
report, and then the part most people skip, reproduce and verify before it ships.

Right now that work lives inside the Metasploit Framework, where I was selected for
Google Summer of Code 2026.

I work from one belief, and it is the line in the banner above: "A Great exploit user can
run an masterpiece, but a masterpiece can build the exploit itself!" Running someone
else's tool is a skill. Building the tool that writes the next exploit is the craft I am
after.

### What I care about

- **Reliable offensive tooling.** An exploit is only as good as the number of times it
  works on a machine that is not mine. I optimize for reproducibility, clear output, and
  code that the next person can maintain.
- **Reading systems until they break.** I did a long stretch of reverse engineering and
  protocol work, and I cannot stop. Once you have watched enough parsers and auth flows
  fail, you build everything differently.
- **Contributing upstream, in the open.** I would rather land one reviewed change in a
  tool thousands of people use than keep a hundred private scripts. Working in public is
  also the best way I know to find people who care about the same problems.

### Metasploit Framework · GSoC 2026 · Rapid7

Mentored by [@jheysel-r7](https://github.com/jheysel-r7) and
[@zeroSteiner](https://github.com/zeroSteiner). I passed the final evaluation; the work
below shipped to [`rapid7/metasploit-framework`](https://github.com/rapid7/metasploit-framework)
and [`rapid7/ruby_smb`](https://github.com/rapid7/ruby_smb) during and after the program.

Two things landed. The first is the full `CertificateTracePresenter` inline-tracing
stack, which brings X.509 visibility into `msfconsole` across 10+ ADCS modules and four
TLS protocols. The second is the first native Kerberos authentication relay framework in
Metasploit (CVE-2026-20929), including the ESC8 AD CS Web Enrollment relay target and
the native IPv6 RA + RDNSS DNS-takeover coercion that drives it. The companion
`ruby_smb` GSS provider change that unblocked the stack upstream merged too.

<table>
<tr><th>PR</th><th>What landed</th><th>Status</th></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21198">#21198</a></td><td><b>CertificateTracePresenter</b> + shared <code>CertificateTrace</code> mixin, wired into 10+ ADCS modules</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21469">#21469</a></td><td>LDAP Schannel certificate tracing</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21580">#21580</a></td><td>CSR tracing for AD CS enrollment (<code>to_s_csr_*</code>)</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21599">#21599</a></td><td>HTTP TLS peer-cert tracing (Phase 1)</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21607">#21607</a></td><td>LDAP + RDP TLS peer-cert tracing (Phase 2)</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21608">#21608</a></td><td>Postgres TLS + full cert-chain tracing (Phase 3)</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21709">#21709</a></td><td><b>Native Kerberos relay stack + ESC8 AD CS target</b> (CVE-2026-20929)</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21725">#21725</a></td><td>Rogue IPv6 RA + RDNSS DNS-takeover coercion</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21719">#21719</a></td><td>Module metadata-cache race fix</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21784">#21784</a></td><td>DNS forward/cache crash fix</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21853">#21853</a></td><td>Relay-driven DNS poisoning hardening</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/metasploit-framework/pull/21906">#21906</a></td><td>WebEnrollment cert-download crash fix</td><td>Merged</td></tr>
<tr><td><a href="https://github.com/rapid7/ruby_smb/pull/303">ruby_smb #303</a></td><td>Kerberos GSS provider (server offers Kerberos alongside NTLM)</td><td>Merged</td></tr>
</table>

Open follow-ups in review (post-program):
MSF [#21908](https://github.com/rapid7/metasploit-framework/pull/21908),
[#21920](https://github.com/rapid7/metasploit-framework/pull/21920),
[#21931](https://github.com/rapid7/metasploit-framework/pull/21931),
[#21934](https://github.com/rapid7/metasploit-framework/pull/21934),
[#21944](https://github.com/rapid7/metasploit-framework/pull/21944) ·
ruby_smb [#306](https://github.com/rapid7/ruby_smb/pull/306),
[#307](https://github.com/rapid7/ruby_smb/pull/307),
[#309](https://github.com/rapid7/ruby_smb/pull/309),
[#310](https://github.com/rapid7/ruby_smb/pull/310).

Credited across **8 Rapid7 Metasploit wrap-up posts** between June and October 2026.
Full build log, lab proof, and timeline live at
[pushpenderrathore.github.io/gsoc.html](https://pushpenderrathore.github.io/gsoc.html).

### Other work

**[Unified Security Operations Framework](https://github.com/Pushpenderrathore/Unified-Security-Operations-Framework)**
A modular SOC pipeline that ties multiple security capabilities into one operational
workflow, so detection, analysis, and response live in one place instead of a drawer of
disconnected scripts.

**[payload_framework](https://github.com/Pushpenderrathore/payload_framework)**
An offensive payload generation and management framework for red-team operations, built
around repeatability rather than one-off generation.

**[Goblins](https://github.com/Pushpenderrathore/Goblins)**
An autonomous security agent that analyzes lab results and publishes its findings as a
running daemon, so the analysis loop keeps going without me.

**[Contractsd](https://github.com/Pushpenderrathore/Contractsd)**
An AES-256-GCM command-line contacts vault, with keys derived through PBKDF2-HMAC-SHA256
at 150k iterations and a per-entry salt. A small tool, taken seriously.

<details>
  <summary><b>More projects (earlier and experimental work)</b></summary>

<br/>

**[shydun](https://github.com/Pushpenderrathore/shydun)**
An SSH-based networking primitive in C, written for security research and adversary
emulation.

**[macchanger_daeion](https://github.com/Pushpenderrathore/macchanger_daeion)**
A systemd service that rotates MAC addresses on a schedule with a privacy kill-switch,
packaged for Arch, Debian, and Fedora.

**[Venice-firewall](https://github.com/Pushpenderrathore/Venice-firewall)**
A firewall that does real-time traffic anomaly analysis with adaptive filtering.

**[LUKS2-nuke](https://github.com/Pushpenderrathore/LUKS2-nuke)**
An anti-forensics wipe of a LUKS2 system after repeated failed decryption attempts.

</details>

### How I work

Languages I reach for: C, C++, Python, and Ruby, with x86 and x64 assembly when I need to
see what the machine is really doing. Daily toolchain: Ghidra, GDB, Binary Ninja,
Wireshark, Nmap, Burp Suite, and Metasploit. Tests in RSpec, because a module without a
spec is a claim without a proof.

### Where I practice

[HackTheBox](https://app.hackthebox.com/public/users/724136) ·
[TryHackMe](https://tryhackme.com/p/enp7s0d) ·
[WeChall](https://www.wechall.net/profile/rootanonymous) ·
[OverTheWire](https://overthewire.org/wargames/)

### Connect

[Portfolio](https://pushpenderrathore.github.io/) ·
[LinkedIn](https://www.linkedin.com/in/pushpender-singh-rathore-72466a260/) ·
[Email](mailto:enp7s0d@gmail.com) ·
[All repositories](https://github.com/Pushpenderrathore?tab=repositories)
