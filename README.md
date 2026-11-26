<p align="center">
  <img src="assets/banner.svg" width="100%" alt="Terminal window titled Cybersecurity Journey: learning, practising and documenting my path into security">
</p>

<p align="center">
  <a href="LICENSE"><img src="assets/badges/license-mit.svg" alt="License: MIT"></a>
  <img src="assets/badges/lang-python.svg" alt="Language: Python">
  <img src="assets/badges/lang-cpp.svg" alt="Language: C++">
  <img src="assets/badges/shell-bash.svg" alt="Shell: Bash">
  <img src="assets/badges/os-linux.svg" alt="OS: Linux">
</p>

<p align="center">
  <a href="#about">About</a> &nbsp;·&nbsp;
  <a href="#learning-areas">Learning Areas</a> &nbsp;·&nbsp;
  <a href="ROADMAP.md">Roadmap</a> &nbsp;·&nbsp;
  <a href="#ethics">Ethics</a> &nbsp;·&nbsp;
  <a href="#contact">Contact</a>
</p>

<img src="assets/divider.svg" width="100%" alt="">

## About

I am a university student working toward a career in cybersecurity. This repository is where I document what I learn and build along the way.

It is organized by learning area and grows as I study, practise and complete my own work. My plan is in [ROADMAP.md](ROADMAP.md).

<img src="assets/divider.svg" width="100%" alt="">

## Learning Areas

Each area is colour-coded by category.

<p>
  <img src="assets/badges/category-fundamentals.svg" alt="Fundamentals">
  <img src="assets/badges/category-networking.svg" alt="Networking">
  <img src="assets/badges/category-operating-systems.svg" alt="Operating Systems">
  <img src="assets/badges/category-programming.svg" alt="Programming">
  <img src="assets/badges/category-security.svg" alt="Security">
  <img src="assets/badges/category-labs-projects.svg" alt="Labs and Projects">
  <img src="assets/badges/category-resources.svg" alt="Certifications and Resources">
</p>

```mermaid
flowchart LR
    F["01 Fundamentals"]:::green --> N["02 Networking"]:::blue
    F --> O["03 Operating Systems"]:::purple
    F --> P["04 Programming"]:::yellow
    N --> S["05-12 Security"]:::red
    O --> S
    P --> S
    S --> L["13-16 Labs and Projects"]:::aqua
    L --> R["17-18 Certifications and Resources"]:::orange

    classDef green fill:#B8BB26,stroke:#79740E,color:#282828
    classDef blue fill:#83A598,stroke:#076678,color:#282828
    classDef purple fill:#D3869B,stroke:#8F3F71,color:#282828
    classDef yellow fill:#FABD2F,stroke:#B57614,color:#282828
    classDef red fill:#FB4934,stroke:#9D0006,color:#282828
    classDef aqua fill:#8EC07C,stroke:#427B58,color:#282828
    classDef orange fill:#FE8019,stroke:#AF3A03,color:#282828
```

| # | Area | Category | Purpose |
| :-: | --- | --- | --- |
| `01` | [Fundamentals](01-Fundamentals/) | <img src="assets/badges/category-fundamentals.svg" alt="Fundamentals"> | Documents my learning in computer science and security fundamentals. |
| `02` | [Networking](02-Networking/) | <img src="assets/badges/category-networking.svg" alt="Networking"> | Documents my learning and practical experience in computer networking and network security. |
| `03` | [Operating Systems](03-Operating-Systems/) | <img src="assets/badges/category-operating-systems.svg" alt="Operating Systems"> | Documents my learning and practical experience with operating systems and their security. |
| `04` | [Programming](04-Programming/) | <img src="assets/badges/category-programming.svg" alt="Programming"> | Contains my programming and scripting work related to cybersecurity. |
| `05` | [Cryptography](05-Cryptography/) | <img src="assets/badges/category-security.svg" alt="Security"> | Documents my learning in cryptography and its practical applications. |
| `06` | [Web Security](06-Web-Security/) | <img src="assets/badges/category-security.svg" alt="Security"> | Documents my learning and practical experience in web and application security. |
| `07` | [Offensive Security](07-Offensive-Security/) | <img src="assets/badges/category-security.svg" alt="Security"> | Documents my learning in offensive security, practised only in authorized environments. |
| `08` | [Defensive Security](08-Defensive-Security/) | <img src="assets/badges/category-security.svg" alt="Security"> | Documents my learning and practical experience in defensive security, monitoring and detection. |
| `09` | [Digital Forensics](09-Digital-Forensics/) | <img src="assets/badges/category-security.svg" alt="Security"> | Documents my learning in digital forensics and incident response. |
| `10` | [Cloud Security](10-Cloud-Security/) | <img src="assets/badges/category-security.svg" alt="Security"> | Documents my learning and practical experience in cloud security. |
| `11` | [Reverse Engineering](11-Reverse-Engineering/) | <img src="assets/badges/category-security.svg" alt="Security"> | Documents my learning in reverse engineering and binary analysis. |
| `12` | [Security Engineering](12-Security-Engineering/) | <img src="assets/badges/category-security.svg" alt="Security"> | Documents my learning in designing and building secure systems. |
| `13` | [CTF Writeups](13-CTF-Writeups/) | <img src="assets/badges/category-labs-projects.svg" alt="Labs and Projects"> | Contains my writeups for capture the flag challenges I attempt. |
| `14` | [Hands-on Labs](14-Hands-on-Labs/) | <img src="assets/badges/category-labs-projects.svg" alt="Labs and Projects"> | Contains my notes and results from practical security labs. |
| `15` | [Projects](15-Projects/) | <img src="assets/badges/category-labs-projects.svg" alt="Labs and Projects"> | Contains the security projects I build. |
| `16` | [Security Research](16-Security-Research/) | <img src="assets/badges/category-labs-projects.svg" alt="Labs and Projects"> | Contains my security research. |
| `17` | [Certifications](17-Certifications/) | <img src="assets/badges/category-resources.svg" alt="Certifications and Resources"> | Documents the certifications I pursue. |
| `18` | [Resources](18-Resources/) | <img src="assets/badges/category-resources.svg" alt="Certifications and Resources"> | Contains resources I have found useful in my learning. |

<img src="assets/divider.svg" width="100%" alt="">

## Ethics

> [!IMPORTANT]
> All security testing documented here is performed only on systems I own or have explicit permission to test, such as personal labs and authorized training platforms. Nothing in this repository is intended for unauthorized or malicious use.

<img src="assets/divider.svg" width="100%" alt="">

## Contact

<p>
  <a href="https://github.com/SuryadevChippada"><img src="assets/badges/contact-github.svg" alt="GitHub: SuryadevChippada"></a>
  <a href="https://www.linkedin.com/in/suryadev-chippada"><img src="assets/badges/contact-linkedin.svg" alt="LinkedIn: suryadev-chippada"></a>
</p>

<img src="assets/divider.svg" width="100%" alt="">

<p align="center"><sub>Maintained by Suryadev Chippada &nbsp;·&nbsp; Released under the <a href="LICENSE">MIT License</a></sub></p>
