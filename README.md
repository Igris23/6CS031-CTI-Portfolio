# 6CS031 Cyber Threat Intelligence – Portfolio Evidence

Sunnatbek Sobirov (2461876), University of Wolverhampton, Semester 1, 2026-27.

The submitted report contains a shortened version of each workshop (500 words maximum). This repository holds the full-length write-up of every workshop and the original evidence.

- [Full-Portfolio.docx](Full-Portfolio.docx) – all four workshops, full version

## Task 1 – Threat Landscape and Intelligence Gathering with Shodan (Week 1)

- [Task1-Shodan-Full.docx](Task1-Shodan/Task1-Shodan-Full.docx) – full write-up

| Figure | Description |
|---|---|
| [Figure 1](Task1-Shodan/screenshots/Figure_01.png) | Search by service: apache. The first banner shows Apache/2.4.29 (Ubuntu), a 2017 release with known CVEs |
| [Figure 2](Task1-Shodan/screenshots/Figure_02.png) | Search by port: port:21. The banner reveals the exact FTP software version (vsFTPd 3.0.3) |
| [Figure 3](Task1-Shodan/screenshots/Figure_03.png) | Search by country: country:"GB". Port 7547 (TR-069 router management) is among the top ports, and one result is in Wolverhampton |
| [Figure 4](Task1-Shodan/screenshots/Figure_04.png) | Combined query. The results include an eol-product tag (PHP 7.3.28) and Apache 2.2.22 last modified in 2014 |
| [Figure 5](Task1-Shodan/screenshots/Figure_05.png) | Host page of an FTP server in Tashkent |
| [Figure 6](Task1-Shodan/screenshots/Figure_06.png) | Query "220" "230 Login successful." port:21: FTP servers that accept anonymous login |
| [Figure 7](Task1-Shodan/screenshots/Figure_07.png) | Query port:502: a Modbus device on a cellular network answers requests for Unit IDs 0, 1 and 255 |
| [Figure 8](Task1-Shodan/screenshots/Figure_08.png) | Query "MongoDB Server Information" port:27017: databases with authentication only partially enabled |

## Task 2 – Person of Interest Investigation with Maltego (Week 2)

- [Task2-Maltego-Full.docx](Task2-Maltego/Task2-Maltego-Full.docx) – full write-up

| Figure | Description |
|---|---|
| [Figure 9](Task2-Maltego/screenshots/Figure_09.png) | Discovery graph for Aina and Marc Clotet |
| [Figure 10](Task2-Maltego/screenshots/Figure_10.png) | Phone numbers and links extracted from ainaclotet.com/i/es/ |
| [Figure 11](Task2-Maltego/screenshots/Figure_11.png) | Verification of the contact details in context |
| [Figure 12](Task2-Maltego/screenshots/Figure_12.png) | Phone numbers extracted from the 2010 archived contact page of marc-clotet.com |
| [Figure 13](Task2-Maltego/screenshots/Figure_13.png) | Funicular Films About Us and Team pages: contact email and linked sites |

## Task 3 – Malware Analysis with ANY.RUN (Week 3)

- [Task3-ANYRUN-Full.docx](Task3-ANYRUN/Task3-ANYRUN-Full.docx) – full write-up

| Figure | Description |
|---|---|
| [Figure 14](Task3-ANYRUN/screenshots/Figure_14.png) | Public submissions for the hash: six runs of the same file, all marked Malicious activity |
| [Figure 15](Task3-ANYRUN/screenshots/Figure_15.png) | Analysis overview: tags agenttesla, stealer, smtp, and the process tree (PID 7544 starts RegSvcs.exe PID 5236) |
| [Figure 16](Task3-ANYRUN/screenshots/Figure_16.png) | Network Threats: Agent Tesla related domain, victim hostname in outbound traffic, SMTP session started |
| [Figure 17](Task3-ANYRUN/screenshots/Figure_17.png) | Connections (whitelisted traffic hidden): RegSvcs.exe connects to 107.178.108.41 on port 587 |
| [Figure 18](Task3-ANYRUN/screenshots/Figure_18.png) | DNS Requests: mail.pgsu.co.id resolves to 107.178.108.41 |
| [Figure 19](Task3-ANYRUN/screenshots/Figure_19.png) | RegSvcs.exe (PID 5236): Agent Tesla found by YARA in a memory dump, with mapped ATT&CK techniques |
| [Figure 20](Task3-ANYRUN/screenshots/Figure_20.png) | Extracted malware configuration: SMTP host, port, username and password |
| [Figure 21](Task3-ANYRUN/screenshots/Figure_21.png) | ANY.RUN MITRE ATT&CK matrix: 5 tactics, 9 techniques |
| [Figure 22](Task3-ANYRUN/screenshots/Figure_22.png) | Sample 1 overview: tags dcrat, rat, backdoor, stealer, and the chain of dropped executables |
| [Figure 23](Task3-ANYRUN/screenshots/Figure_23.png) | 1.exe (PID 6704) detected as DCRat, with several schtasks.exe processes below it |
| [Figure 24](Task3-ANYRUN/screenshots/Figure_24.png) | HTTP Requests: PLUGScheduler.exe sends a POST to the C2 URL on nyashtech.top |
| [Figure 25](Task3-ANYRUN/screenshots/Figure_25.png) | Connections filtered by PID 6384: the C2 domain resolves to 104.21.31.169 (Cloudflare) |
| [Figure 26](Task3-ANYRUN/screenshots/Figure_26.png) | Network Threats: DarkCrystal RAT check-in detected |
| [Figure 27](Task3-ANYRUN/screenshots/Figure_27.png) | ANY.RUN MITRE ATT&CK matrix for sample 1: 4 tactics, 8 techniques |
| [Figure 28](Task3-ANYRUN/screenshots/Figure_28.png) | VirusTotal detection: 61/71 engines, popular threat label trojan.sfuzuan/midie |
| [Figure 29](Task3-ANYRUN/screenshots/Figure_29.png) | Basic properties: hashes, imphash and file type of sample 2 |
| [Figure 30](Task3-ANYRUN/screenshots/Figure_30.png) | Network communication: DNS-over-HTTP lookups through 223.5.5.5 and connections to Chinese cloud services |
| [Figure 31](Task3-ANYRUN/screenshots/Figure_31.png) | Registry changes to network (DHCP/Tcpip) settings and processes created, including randomly named files in SysWOW64 |
| [Figure 32](Task3-ANYRUN/screenshots/Figure_32.png) | Sigma and IDS rule matches: suspicious file extension, IE registry change, .top DNS queries, DNS over HTTPS |
| [Figure 33](Task3-ANYRUN/screenshots/Figure_33.png) | VirusTotal MITRE ATT&CK mapping for sample 2 |

## Task 4 – Threat Modelling with the Microsoft Threat Modelling Tool (Week 4)

- [Task4-ThreatModelling-Full.docx](Task4-ThreatModelling/Task4-ThreatModelling-Full.docx) – full write-up
- [VLE_Portal.tm7](Task4-ThreatModelling/VLE_Portal.tm7) – Threat model file (open in Microsoft Threat Modeling Tool 7.3)
- [VLE_report.htm](Task4-ThreatModelling/VLE_report.htm) – Full HTML report generated by the tool
- [VLE_threats.csv](Task4-ThreatModelling/VLE_threats.csv) – All 80 generated threats exported as CSV

| Figure | Description |
|---|---|
| [Figure 34](Task4-ThreatModelling/screenshots/Figure_34.png) | Data flow diagram of the student/staff portal in the Microsoft Threat Modelling Tool |
| [Figure 35](Task4-ThreatModelling/screenshots/Figure_35.png) | Threats generated in the Analysis View |
| [Figure 36](Task4-ThreatModelling/screenshots/Figure_36.png) | Threat 27 (Information Disclosure) set to Mitigated with a justification |
| [Figure 37](Task4-ThreatModelling/screenshots/Figure_37.png) | Full report generated by the Threat Modelling Tool |

## Note

All data comes from public sources (Shodan index, public websites, Wayback Machine, public ANY.RUN and VirusTotal reports). IP addresses are partly masked. No system was accessed or logged in to.
