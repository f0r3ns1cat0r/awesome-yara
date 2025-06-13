<p align="center">
  <img height="128" src="./awesome-yara.png"  alt="Awesome YARA" title="Awesome YARA">
</p>

<h1 align="center">Awesome YARA</h1>

A curated list of awesome YARA rules, tools, and resources. Inspired by [awesome-python](https://github.com/vinta/awesome-python) and [awesome-php](https://github.com/ziadoz/awesome-php).

> YARA is an ancronym for: YARA: Another Recursive Ancronym, or Yet Another Ridiculous Acronym. Pick your choice.
>
> -- *[Victor M. Alvarez (@plusvic)](https://twitter.com/plusvic/status/778983467627479040)*

[YARA](https://virustotal.github.io/yara/), the "pattern matching swiss knife for malware researchers (and everyone else)" is developed by [@plusvic](https://github.com/plusvic/) and [@VirusTotal](https://github.com/VirusTotal). View it on [GitHub](https://github.com/virustotal/yara).

### Contents

- [100 Days of YARA (#100DaysofYARA)](#100-days-of-yara-100daysofyara)
- [Guides](#guides)
- [Rules](#rules)
- [Tools](#tools)
- [Services](#services)
- [Syntax Highlighters](#syntax-highlighters)
- [People](#people)
- [Videos and Talks](#videos-and-talks)
- [Related Awesome Lists](#related-awesome-lists)
- [Contributing](#contributing)
  - [Contributors](#contributors)

### Legend

* :eyes: - Actively maintained, a repository worth watching.
* :gem: - Novel, interesting, educational, or otherwise stand-out content.
* :sparkles: - Added more recently, shiny new toys.
* :trophy: - The biggest collection award, awarded to a single repo.

## 100 Days of YARA (#100DaysofYARA)
An annual YARA challenge started by [Greg Lesnewich](https://twitter.com/greglesnewich) in 2022, inspired by #100DaysOfCode and taking place in the first 100 days of the year. The goal is to contribute daily to the YARA community through rule creation, source code contributions, or generally teaching/help your colleagues. Other key contributors include [Wesley Shields](https://twitter.com/wxs) and [Steve Miller](https://twitter.com/stvemillertime). For a list of all participants in the first two years of the challenge, see our [Twitter List](https://twitter.com/i/lists/1648861278901764096).

Rule collections from prior years of the challenge: [100 Days of YARA](https://github.com/100DaysofYARA)

## Guides

* [Yara Performance Guidelines](https://github.com/Neo23x0/YARA-Performance-Guidelines)
* [YARA-Style-Guide](https://github.com/Neo23x0/YARA-Style-Guide)

## Rules

* [AlienVault Labs Rules](https://github.com/AlienVault-Labs/AlienVaultLabs/tree/master/malware_analysis)
    - Collection of tools, signatures, and rules from the researchers at [AlienVault Labs](https://cybersecurity.att.com/blogs/labs-research). Search the repo for .yar and .yara extensions to find about two dozen rules ranging from APT detection to generic sandbox / VM detection. Last updated in January of 2016.
* [anyrun rules](https://github.com/anyrun/YARA)
    - Public YARA rules
* [Apple OSX](https://gist.github.com/pedramamini/c586a151a978f971b70412ca4485c491)
    - Apple has ~40 YARA signatures for detecting malware on OSX. The file, XProtect.yara, is available locally at /System/Library/CoreServices/XProtect.bundle/Contents/Resources/.
* [bartblaze YARA rules](https://github.com/bartblaze/Yara-rules) :eyes:
    - Collection of personal YARA rules
* [BinaryAlert YARA Rules](https://github.com/airbnb/binaryalert/tree/master/rules/public)
    - A couple dozen rules written and released by AirBnB as part of their BinaryAlert tool (see next section). Detection for hack tools, malware, and ransomware across Linux, Window, and OS X. This is a new and active project.
* [Burp YARA Rules](https://github.com/codewatchorg/Burp-Yara-Rules)
    - Collection of YARA rules intended to be used with the Burp Proxy through the Yara-Scanner extension. These rules focus mostly on non-exe malware typically delivered over HTTP including HTML, Java, Flash, Office, PDF, etc. Last updated in June of 2016.
* [BinSequencer](https://github.com/karttoon/binsequencer)
    - Find a common pattern of bytes within a set of samples and generate a YARA rule from the identified pattern.
* [CAPE Rules](https://github.com/kevoreilly/CAPEv2/tree/master/data/yara) :eyes:
    - Rules from various authors bundled with the Config And Payload Extraction Cuckoo Sandbox extension (see next section).
* [CDI Rules](https://github.com/CyberDefenses/CDI_yara)
    - Collection of YARA rules released by [CyberDefenses](https://cyberdefenses.com/blog/) for public use. Built from information in intelligence profiles, dossiers and file work.
* [Citizen Lab Malware Signatures](https://github.com/citizenlab/malware-signatures)
    - YARA signatures developed by Citizen Lab. Dozens of signatures covering a variety of malware families. The also inclde a syntax file for Vim. Last update was in November of 2016.
* [ConventionEngine Rules](https://github.com/stvemillertime/ConventionEngine) :sparkles:
    - A collection of Yara rules looking for PEs with PDB paths that have unique, unusual, or overtly malicious-looking keywords, terms, or other features.
* [Deadbits Rules](https://github.com/deadbits/yara-rules) :eyes:
    - A collection of YARA rules made public by [Adam Swanda](https://www.deadbits.org/), Splunk's Principal Threat Intel. Analyst, from his own recent malware research.
* [Delivr.to Detections](https://github.com/delivr-to/detections)
    - This repo serves as a home for detection content developed by the delivr.to team.
* [Didier Stevens Rules](https://github.com/DidierStevens/DidierStevensSuite) :gem:
    - Collection of rules from Didier Stevens, author of a suite of tools for inspecting OLE/RTF/PDF. Didier's rules are worth scrutinizing and are generally written purposed towards hunting. New rules are frequently announced through the [NVISO Labs Blog](https://blog.nviso.eu/).
* [Ditekshen Rules](https://github.com/ditekshen/detection)
    - A set of interrelated network and host detection rules with the aim of improving detection and hunting visibility and context.
* [Elastic Security YARA Rules](https://github.com/elastic/protections-artifacts/tree/main/yara)
    - Elastic Security provides signature-based YARA rules within the Elastic Endpoint product. These rules are used to detect and prevent emerging threats within Linux, Windows, and macOS systems. Our repository holds over 1,000 YARA rules that are used every day to stop a wide range of threats including: Trojans, ransomware, cryptominers, attack penetration frameworks, and more.
* [ESET IOCs](https://github.com/eset/malware-ioc/) :eyes:
    - Collection of YARA and Snort rules from IOCs collected by ESET researchers. There's about a dozen YARA Rules to glean from in this repo, search for file extension .yar. This repository is seemingly updated on a roughly monthly interval. New IOCs are often mentioned on the [ESET WeLiveSecurity Blog](https://www.welivesecurity.com/).
* [Fidelis Rules](https://github.com/fideliscyber/indicators/tree/master/yararules)
    - You can find a half dozen YARA rules in Fidelis Cyber's IOC repository. They update this repository on a roughly quarterly interval. Complete blog content is also available in this repository.
* [Filescan.io Rules](https://github.com/filescanio/fsYara) ✨
    - A collection of curated YARA rules used as part of the Filescan.io service.
* [FireEye](https://github.com/fireeye/red_team_tool_countermeasures)
    - FireEye Red Team countermeasures detection
* [Florian Roth Rules](https://github.com/Neo23x0/signature-base/tree/master/yara) :eyes: :gem:
    - Florian Roth's signature base is a frequently updated collection of IOCs and YARA rules that cover a wide range of threats. There are dozens of rules which are actively maintained. Watch the repository to see rules evolve over time to address false positives / negatives.
* [Florian Roth's IDDQD Rule](https://gist.github.com/Neo23x0/f1bb645a4f715cb499150c5a14d82b44)
    - A proof-of-concept rule that shows how easy it actually is to detect red teamer and threat group tools and code.
* [f0wl yara_rules](https://github.com/f0wl/yara_rules)
    - A collection of Yara rules from https://dissectingmalwa.re/ blog posts.
* [Frank Boldewin's Rules](https://github.com/fboldewin/YARA-rules)
    - A collection of YARA Rules from [@r3c0nst](https://twitter.com/@r3c0nst).
* [FSF Rules](https://github.com/EmersonElectricCo/fsf/tree/master/fsf-server/yara)
    - Mostly filetype detection rules, from the EmersonElectricCo FSF project (see next section).
* [GoDaddy ProcFilter Rules](https://github.com/godaddy/yara-rules)
    - A couple dozen rules written and released by GoDaddy for use with ProcFilter (see next section). Example rules include detection for packers, mimikatz, and specific malware.
* [Google Cloud Threat Intelligence(GCTI) Rules](https://github.com/chronicle/GCTI)
    - Rules to detect CobaltStrike framework and Sliver implant.
* [h3x2b Rules](https://github.com/h3x2b/yara-rules) :gem:
    - Collection of signatures from h3x2b which stand out in that they are generic and can be used to assist in reverse engineering. There are YARA rules for identifying crypto routines, highly entropic sections (certificate discovery for example), discovering injection / hooking functionality, and more.
* [HydraDragonAntivirus](https://github.com/HydraDragonAntivirus/HydraDragonAntivirus) :trophy:
    - World's largest open source YARA collection with no duplicates, no invalid ones and only few files. Also it contains ClamAV + YARA-X or YARA + Machine Learning + IDS canner and signatures and SUBLIME + CAPA + SIGMA signatures. Finally it has so big malware collection.
* [Icewater Rules](https://github.com/SupportIntelligence/Icewater)
    - Repository of automatically generated YARA rules from Icewater.io. This repository is updated rapidly with newly generated signatures that mostly match on file size range and partial content hashes.
* [imp0rtp3's Rules](https://github.com/imp0rtp3/yara-rules)
    - A small repository which contains some browser based rules.
* [Intezer Rules](https://github.com/intezer/yara-rules) :sparkles:
    - YARA rules published by Intezer Labs.
* [InQuest Rules](https://github.com/InQuest/yara-rules) :eyes:
    - YARA rules published by InQuest researchers mostly geared towards threat hunting on Virus Total. Rules are updated as new samples are collected and novel pivots are discovered. The [InQuest Blog](http://blog.inquest.net) will often discuss new findings.
* [jeFF0Falltrades Rules](https://github.com/jeFF0Falltrades/YARA-Signatures) :sparkles:
    - A collection of YARA signatures for various malware families.
* [kevthehermit Rules](https://github.com/kevthehermit/YaraRules)
    - Dozens of rules from the personal collection of Kevin Breen. This repository hasn't been updated since February of 2016.
* [Loginsoft Rules](https://research.loginsoft.com/yara-rules/)
    - Yara Rules for Detecting Malicious Documents targeting Microsoft Office format.
* [lw-yara](https://github.com/Hestat/lw-yara)
    - Ruleset for scanning Linux servers for shells, spamming, phishing and other webserver baddies.
* [ndaal_YARA_passwords_default](https://gitlab.com/ndaal_open_source/ndaal_yara_passwords_default)
    - YARA rules includes default credentials of at least 1043 organizations which are hashed with different hash permutations such as base64, md5, sha512, etc.
* [ndaal_YARA_passwords_weak](https://gitlab.com/ndaal_open_source/ndaal_yara_passwords_weak)
    - YARA rules includes hashed passwords of the top weak passwords. The passwords are hashed in a respective rule according to the following permutations such as base64, md5, sha512, etc.
* [NCC Group Rules](https://github.com/nccgroup/Cyber-Defence/tree/master/Signatures/yara) :eyes:
    - A handful of YARA rules released by NCC Group's Cyber Defence team.
* [MalGamy's YARA_Rules](https://github.com/MalGamy/YARA_Rules)
    - A small repository which contains some stealer rules.
* [Malice.IO YARA Plugin Rules](https://github.com/malice-plugins/yara/tree/master/rules) :eyes:
    - Collection of topical from a variety of sources for the YARA component of the Malice.IO framework.
* [Malpedia Auto Generated Rules](https://malpedia.caad.fkie.fraunhofer.de/api/get/yara/auto/zip) :sparkles:
    - A zip file that contains all automatically generated, code-based rules created using Malpedia's YARA-Signator
* [Malpedia Auto Generated Rules Repo](https://github.com/malpedia/signator-rules) :sparkles:
    - Repository to simplify access to and synchronization of Malpedia's automatically generated, code-based YARA rules.
* [McAfee Advanced Threat Research IOCs](https://github.com/advanced-threat-research/IOCs)
    - IOCs, including YARA rules, to accompany McAfee ATR's blog and other public posts.
* [McAfee Advanced Threat Research Yara-Rules](https://github.com/advanced-threat-research/Yara-Rules)
    - Repository of YARA rules made by McAfee ATR Teams.
* [mikesxrs YARA Rules Collection](https://github.com/mikesxrs/Open-Source-YARA-rules) :eyes:
    - Large collection of open source rules aggregated from a variety of sources, including blogs and other more ephemeral sources. Over 100 categories, 1500 files, 4000 rules, and 20Mb. If you're going to pull down a single repo to play with, this is the one.
* [Public YARA Rules](https://github.com/jipegit/yara-rules-public)
    - Repository of Public YARA Rules.
* [QuickSand Lite Rules](https://github.com/tylabs/quicksand_lite)
    - This repo contains a C framework and standalone tool for malware analysis, along with several useful YARA rules developed for use with the project.
* [Rapid7-Labs](https://github.com/rapid7/Rapid7-Labs/)
    - This repository contains a curated collection of Sigma & Yara rules and Indicators of Compromise (IOCs) shared by Rapid7 Labs.
* [Rastrea2r](https://github.com/rastrea2r/rastrea2r)
    - Triage suspect systems and hunt for Indicators of Compromise (IOCs) across thousands of endpoints in minutes.
* [ReversingLabs YARA Rules](https://github.com/reversinglabs/reversinglabs-yara-rules) :sparkles: :eyes:
    - A collection of yara rules published by ReversingLabs which covers exploits, infostealers, ransomware, trojans, and viruses. 
* [Securitymagic's YARA Rules](https://github.com/securitymagic/yara)
    - YARA rules for a variety of threats.
* [Sophos AI YaraML Rules](https://github.com/inv-ds-research/yaraml_rules)
    - A repository of Yara rules created automatically as translations of machine learning models. Each directory will have a rule and accompanying metadata: hashes of files used in training, and an accuracy diagram (a ROC curve).
* [SpiderLabs Rules](https://github.com/SpiderLabs/malware-analysis/tree/master/Yara)
    - Repository of tools and scripts related to malware analysis from the researchers at SpiderLabs. There's only three YARA rules here and the last update was back in 2015, but worth exploring.
* [StrangeRealIntel's Daily IOCs](https://github.com/StrangerealIntel/DailyIOC) :gem: :sparkles: :eyes:
    - Regularly updated YARA rules covering a variety of fresh threats.
* [t4d's PhishingKit-Yara-Rules](https://github.com/t4d/PhishingKit-Yara-Rules)
    - This repository, dedicated to Phishing Kits zip files YARA rules, is based on zip raw format analysis to find directories and files names, you don't need yara-extend there.
* [Telekom Security Malare Analysis Repository](https://github.com/telekom-security/malware_analysis)
    - This repository comprises scripts, signatures, and additional IOCs of our blog posts at the telekom.com blog.
* [Tenable Rules](https://github.com/tenable/yara-rules)
    - Small collection from Tenable Network Security.
* [ThreatHunting-Keywords-yara-rules](https://github.com/mthcht/ThreatHunting-Keywords-yara-rules)
    - Yara rules for Threat Hunting sessions
* [TjadaNel Rules](https://github.com/tjnel/yara_repo)
    - Small collection of malware rules.
* [VectraThreatLab Rules](https://github.com/VectraThreatLab/reyara)
    - YARA rules for identifying anti-RE malware techniques.
* [Volexity - Threat-Intel](https://github.com/volexity/threat-intel) :sparkles: :gem:
    - This repository contains IoCs related to Volexity public threat intelligence blog posts.
* [x64dbg Signatures](https://github.com/x64dbg/yarasigs) :gem:
    - Collection of interesting packer, compiler, and crypto identification signatures.
* [YAIDS](https://github.com/wrayjustin/yaids) :gem: :sparkles:
    - YAIDS is a Multi-Threaded Intrusion Detection System using Yara. YAIDS supports all valid Yara rules (including modules) and any PCAP compatible data stream (Network, USB, Bluetooth, etc.).
* [YARA-FORENSICS](https://github.com/Xumeiquer/yara-forensics)
    - Collection of file type identifying rules.
* [YARA Forge](https://yarahq.github.io/) :gem: :sparkles: :eyes:
    - YARA Forge specializes in delivering high-quality YARA rule packages for immediate integration into security platforms.
* [yara4pentesters](https://github.com/DiabloHorn/yara4pentesters)
    - Rules to identify files containing juicy information like usernames, passwords etc.
* [YaraRules Project Official Repo](https://github.com/Yara-Rules/rules) :eyes:
    - Large collection of rules constantly updated by the community.
* [Yara-Unprotect](https://github.com/fr0gger/Yara-Unprotect)
    - Rules created for the Unprotect Project for detecting malware evasion techniques.
    * [Unprotect Project](https://unprotect.it/detection-rules/)
      -   Detection Rule List.

## Tools

* [AirBnB BinaryAlert](https://github.com/airbnb/binaryalert)
    - Open-source serverless AWS pipeline where any file uploaded to an S3 bucket is immediately scanned with a configurable set of YARA rules.
* [alterix](https://github.com/mtnmunuklu/alterix)
    - Converts Yara rules to the query language of CRYPTTECH's SIEM
* [androguard-yara](https://github.com/MindMac/androguard-yara)
    - Androguard module for Yara.
* [APKiD](https://github.com/rednaga/APKiD)
    - Android Application Identifier for Packers, Protectors, Obfuscators and Oddities - PEiD for Android
* [a-ray-grass](https://github.com/hashlookup/a-ray-grass)
    - YARA module that provides support for bloom filters in yara. In the context of [hashlookup.io](https://hashlookup.io/), it allows to quickly discard known files before any further analysis.
* [Arya- The Reverse YARA](https://github.com/claroty/arya)
    - Arya is a unique tool that produces pseudo-malicious files meant to trigger YARA rules. You can think of it like a reverse YARA because it does exactly the opposite - it creates files that matches your rules.
* [Audit Node Modules With YARA Rules](https://github.com/rpgeeganage/audit-node-modules-with-yara)
    - Run a given set of YARA rules against the given node_module folder
* [AutoYara](https://github.com/NeuromorphicComputationResearchProgram/AutoYara)
    - Automated Yara Rule generation using Biclustering
* [base64_substring](https://github.com/DissectMalware/base64_substring)
    - Generate YARA rules to match terms against base64-encoded data.
* [bincapz](https://github.com/chainguard-dev/bincapz)
    - Enumerates program capabilities and malicious behaviors using fragment analysis..
* [CAPE: Config And Payload Extraction](https://github.com/kevoreilly/CAPEv2) :eyes:
    - Extension of Cuckoo specifically designed to extract payloads and configuration from malware. CAPE can detect a number of malware techniques or behaviours, as well as specific malware families, from its initial run on a sample. This detection then triggers a second run with a specific package, in order to extract the malware payload and possibly its configuration, for further analysis.
* [CCCS-Yara](https://github.com/CybercentreCanada/CCCS-Yara)
    - YARA rule metadata specification and validation utility.
* [clara](https://github.com/abhinavbom/clara) :sparkles:
    - Serverless, real-time, ClamAV+Yara scanning for your S3 Buckets.
* [Cloudina Security Hawk](https://github.com/cloudina/hawk) :sparkles:
    - Multi Cloud antivirus scanning API based on CLAMAV and YARA for AWS S3, AZURE Blob Storage, GCP Cloud Storage.
* [CrowdStrike Feed Management System](https://github.com/CrowdStrike/CrowdFMS)
    - Framework for automating collection and processing of samples from VirusTotal, and executing commands based on YARA rule matches.
* [CSE-CST AssemblyLine](https://bitbucket.org/cse-assemblyline/alsvc_yara)
    - The Canadian Communications Security Establishment (CSE) open sourced [AssemblyLine](https://cyber.gc.ca/en/assemblyline), a platform for analyzing malicious files. The component linked here provides an interface to YARA.
* [decompressingyara](https://github.com/rjzak/decompressingyara)
    - For when your malware samples are stored compressed, but you still want to run rules against them.
* [dnYara](https://github.com/airbus-cert/dnYara)
    - A multi-platform .NET wrapper library for the native YARA library.
* [ELAT](https://github.com/reed1713/ELAT)
    - Event Log Analysis Tool that creates/uses YARA rules for Windows event log analysis.
* [Emerson File Scanning Framework (FSF)](https://github.com/EmersonElectricCo/fsf)
    - Modular, recursive file scanning solution.
* [ExchangeFilter](https://github.com/k-sec-tools/ExchangeFilter)
    - MS Exchange transport agent uses YARA to detect malware in email messages.
* [factual-rules-generator](https://github.com/CIRCL/factual-rules-generator)
    - Factual-rules-generator is an open source project which aims to generate YARA rules about installed software from a running operating system.
* [Fadavvi YARA collection script](https://github.com/Fadavvi/Yara-Repo)
* [FARA](https://github.com/bartblaze/FARA)
    - FARA, or Faux YARA, is a simple repository that contains a set of purposefully erroneous Yara rules. It is meant as a training vehicle for new security analysts, those that are new to Yara and even Yara veterans that want to keep their rule writing (and debugging) sharp.
* [Fastfinder](https://github.com/codeyourweb/fastfinder)
    - Fast customisable cross-platform suspicious file finder. Designed for incident response. Supports md5/sha1/sha256 hashs, litteral/wildcard strings, regular expressions and YARA rules. Can easily be packed to be deployed on any windows / linux host.
* [findcrypt-yara](https://github.com/polymorf/findcrypt-yara) and [FindYara](https://github.com/OALabs/FindYara)
    - IDA pro plugins to scan your binary with YARA rules to find crypto constants (and more).
* [Fibratus](https://www.fibratus.io)
    - A modern tool for Windows kernel exploration and observability with a focus on security and [support for YARA](https://www.fibratus.io/#/filters/functions?id=yara-functions).
* [Fnord](https://github.com/Neo23x0/Fnord)
    - Pattern extractor for obfuscated code.
* [GoDaddy ProcFilter](https://github.com/godaddy/procfilter) :gem:
    - ProcFilter is a process filtering system for Windows with built-in YARA integration. YARA rules can be instrumented with custom meta tags that tailor its response to rule matches. It runs as a Windows service and is integrated with Microsoft's ETW API, making results viewable in the Windows Event Log. Installation, activation, and removal can be done dynamically and does not require a reboot.
* [GhidraYara](https://github.com/subreption/ghidra_yara)
      - A Ghidra extension providing direct integration of YARA through an analyzer, as well as rule generation from code listings and management in the Ghidra UI. Supports an extensive library of cryptographic constants, CRC tables, etc.
* [go-yara](https://github.com/hillu/go-yara)
    - Go bindings for YARA.
* [halogen](https://github.com/target/halogen)
    - Halogen is a tool to automate the creation of yara rules against image files embedded within a malicious document.
* [Hyara](https://github.com/hyuunnn/Hyara)
    - IDA Pro, Cutter, and BinaryNinja plugin that provides easy creation of YARA rules for ASCII & hex strings between a given start and end address.
* [IDA_scripts](https://github.com/swackhamer/IDA_scripts)
    - IDA Python scripts for generating YARA sigs from executable opcodes (.NET included).
* [ida_yara](https://github.com/alexander-hanel/ida_yara)
    - Scan data within an IDB using YARA.
* [ida-yara-processor](https://github.com/bnbdr/ida-yara-processor)
    - IDA processor for compiled YARA rules.
* [InQuest ThreatKB](https://github.com/InQuest/ThreatKB)
    - Knowledge base workflow management for YARA rules and C2 artifacts (IP, DNS, SSL).
* [iocextract](https://github.com/InQuest/python-iocextract)
    - Advanced Indicator of Compromise (IOC) extractor, with YARA rule extraction.
* [Invoke-Yara](https://github.com/secabstraction/Yara)
    - Powershell scripts to run YARA on remote machines.
* [java2yara](https://github.com/fxb-cocacoding/java2yara)
    - A minimal library to generate YARA rules from JAVA
* [KLara](https://github.com/KasperskyLab/klara)
    - Distributed system written in Python, allows researchers to scan one or more YARA rules over collections with samples.
* [Laika BOSS](https://github.com/lmco/laikaboss)
    - Object scanner and intrusion detection system that strives to achieve the following goals: Scalable, Flexible, Verbose.
    - [Whitepaper](https://github.com/lmco/laikaboss/blob/master/LaikaBOSS_Whitepaper.pdf)
* [libyara.NET](https://github.com/microsoft/libyara.NET)
    - .NET wrapper for libyara built in C++ CLI used to easily incorporate yara into .NET projects
* [Malcat](https://malcat.fr)
    - Hexadecimal editor, disassembler and decompiler for malware analysis. Embeds both a YARA scanner and rule editor for easy in-app rule creation. Free and paid versions are available.
* [MalConfScan](https://github.com/JPCERTCC/MalConfScan)
    - MalConfScan is a Volatility plugin extracts configuration data of known malware. This tool searches for malware in memory images and dumps configuration data. In addition, this tool has a function to list strings to which malicious code refers.
* [malscan](https://github.com/usualsuspect/malscan)
    - Scan process memory for YARA matches and execute Python scripts if a match is found.
* [malwatch](https://github.com/defended-net/malwatch)
    - Fast and lightweight malware scanner written in go that is ideal for Linux based web server environments. Currently used with some of the internet's largest deployments.
* [Manalyzer Yara Validator](https://yaravalidator.manalyzer.org/)
    - Compile your rules on all yara versions online to detect compatibility issues!
* [MISP Threat Sharing](https://github.com/MISP/MISP)
    - Threat intelligence platform including indicators, threat intelligence, malware samples and binaries. Includes support for sharing, generating, and validating YARA signatures.
* [MITRE MultiScanner](https://github.com/mitre/multiscanner)
    - File analysis framework that assists the user in evaluating a set of files by automatically running a suite of tools for the user and aggregating the output.
* [mkYARA](https://github.com/fox-it/mkYARA)
    - Generate YARA rules based on binary code.
* [mquery](https://github.com/CERT-Polska/mquery)
    - Web frontend for running blazingly fast YARA queries on large datasets.
* [ndaal YARA ruleset checker](https://gitlab.com/ndaal_open_source/ndaal_yara_nyc)
    - ndaal YARA ruleset checker, Open Source
* Nextron Systems OSS and Commercial Tools (Florian Roth: @Neo23x0)
    - [Loki](https://github.com/Neo23x0/Loki) IOC and YARA rule scanner implemented in Python. Open source and free.
    - [THOR Lite](https://www.nextron-systems.com/thor-lite/) IOC and YARA rule scanner implemented in Go. Closed source, free, but registration required.
* [node-yara](https://github.com/nospaceships/node-yara)
    - YARA support for Node.js.
* [ocaml-yara](https://github.com/elastic/ocaml-yara)
    - OCaml bindings to libyara
* [OCYara](https://github.com/bandrel/OCyara)
    - Performs OCR on image files and scans them for matches to YARA rules.
* [osquery](https://osquery.readthedocs.io/en/stable/deployment/yara/)
    - YARA-based scanning with osquery.
* [PasteHunter](https://github.com/kevthehermit/PasteHunter)
    - Scan pastebin.com with YARA rules.
* [plast](https://github.com/sk4la/plast)
    - Threat hunting tool for detecting and processing IOCs using YARA under the hood.
* [plyara](https://github.com/plyara/plyara)
    - Parse YARA rules with Python.
* [Polichombr](https://github.com/ANSSI-FR/polichombr)
    - Collaborative malware analysis framework with YARA rule matching and other features.
* [PwC Cyber Threat Operations rtfsig](https://github.com/PwCUK-CTO/rtfsig)
    - This tool is designed to make it easy to signature potentially unique parts of RTF files.
* [VirusTotalTools](https://github.com/silascutler/VirusTotalTools)
    - Tools for checking samples against Virus Total, including VT_RuleMGR, for managing threat hunting YARA rules.
* [shotgunyara](https://github.com/darienhuss/shotgunyara)
    - Given a string, create 255 xor encoded versions of that string as a YARA rule.
* [spyre](https://github.com/spyre-project/spyre)
    - Simple, self-contained YARA-based file IOC scanner.
* [static_file_analysis](https://github.com/lprat/static_file_analysis)
    - Analyze deeply embedded files (doc, pdf, exe, ...) with clamscan and YARA.
* [stoQ](https://github.com/PUNCH-Cyber/stoq)
    - Modular and highly customizable framework for the creation of data sets from multiple disparate data sources.
* [Strelka](https://github.com/target/strelka)
    - Detection-Oriented File Analysis System built on Python3, ZeroMQ, and YARA, primarily used for threat detection/hunting and intelligence gathering.
* [Sysmon EDR](https://github.com/ion-storm/sysmon-edr) :sparkles:
    - YARA scanning, process killing, network blocking, and more.
* [SwishDbgExt](https://github.com/comaeio/SwishDbgExt)
    - Microsoft WinDbg extension which includes the ability to use YARA rules to hunt processes in memory.
* [ThreatIngestor](https://github.com/InQuest/ThreatIngestor/)
    - Automatically extract and aggregate IOCs including YARA rules from many sources.
* [UXProtect](https://digitasecurity.com/uxprotect/)
    - The missing UI to Apple's built-in XProtect YARA signatures. Enumerate signatures, scan files, and more.
* [VTCodeSimilarity-YaraGen](https://github.com/arieljt/VTCodeSimilarity-YaraGen) :gem: :sparkles:
    - Yara rule generator using VirusTotal code similarity feature `code-similar-to:` written by [@arieljt](https://twitter.com/arieljt).
* [Vxsig](https://github.com/google/vxsig) :sparkles:
    - Automatically generate AV byte signatures from sets of similar binaries.
* [yabin](https://github.com/AlienVault-OTX/yabin)
    - Creates YARA signatures from executable code within malware.
* [yaml2yara](https://github.com/nccgroup/yaml2yara)
    - Generate bulk YARA rules from YAML input.
* [YARA-CI](https://yara-ci.cloud.virustotal.com/) :sparkles:
    - YARA-CI helps you to keep your YARA rules in good shape. It can be integrated into any GitHub
* [yaradbg-backend](https://github.com/DissectMalware/yaradbg-backend) :gem:
    - YaraDbg is a free web-based Yara debugger to help security analysts to write hunting or detection rules with less effort and more confidence.
* [yaradbg-frontend](https://github.com/DissectMalware/yaradbg-frontend) :eyes:
    - YaraDbg is a free web-based Yara debugger to help security analysts to write hunting or detection rules with less effort and more confidence. 
* [yara-endpoint](https://github.com/Yara-Rules/yara-endpoint)
    -  Tool useful for incident response as well as anti-malware enpoint based on YARA signatures.
* [YaraFileCheckerLib](https://github.com/k-sec-tools/YaraFileCheckerLib)
    - .Net Library designed to make it easier to check potentially malicious files and archives using YARA and make a decision about their harmfulness based on the weights of the detected rules.
* [YaraGenerator](https://github.com/Xen0ph0n/YaraGenerator)
    - Quick, simple, and effective yara rule creation to isolate malware families and other malicious objects of interest.
* [YaraGen](https://github.com/mrexodia/YaraGen) and [yara_fn](https://github.com/williballenthin/idawilli/tree/master/scripts/yara_fn)
    - Plugins for x64dbg and IDAPython, respectively, that generate YARA rules from function blocks.
* [YaraGuardian](https://github.com/PUNCH-Cyber/YaraGuardian)
    - Django web interface for managing YARA rules.
* [YaraHunter](https://github.com/deepfence/YaraHunter)
    - Malware scanner for cloud-native, as part of CI/CD and at Runtime
* [yara-java](https://github.com/subreption/yara-java)
    - Java bindings for YARA (Subreption fork, maintained as of 2024, [old bindings](https://github.com/p8a/yara-java)).
* [yaralyzer](https://github.com/michelcrypt4d4mus/yaralyzer)
    - Visually inspect and force decode YARA and regex matches found in both binary and text data. With Colors.
* [yaramail](https://seanthegeek.github.io/yaramail/)
    - A YARA scanner designed for phishing triage automation. Categorizes emails email authentication, attachments, and normalized body content.  
* [yaraMail](https://github.com/kevthehermit/yaraMail)
    - YARA scanner for IMAP feeds and saved streams.
* [Yara Malware Quick menu scanner](https://github.com/techbliss/Yara_Mailware_Quick_menu_scanner)
    - Adds the awsome YARA pattern scanner to Windows right click menus.
* [YaraManager](https://github.com/kevthehermit/YaraManager)
    - Web based manager for YARA rules.
* [Yaramanager](https://github.com/3c7/yaramanager) ([PyPI](https://pypi.org/project/yaramanager/))
    - Command line tool to manage and organize your Yara ruleset.
* [yaramod](https://github.com/avast/yaramod)
    - A library that provides parsing of YARA rules into AST and a C++ programming interface to build new YARA rulesets.
* [yarAnalyzer](https://github.com/Neo23x0/yarAnalyzer)
    - YARA rule set coverage analyzer.
* [yara-ocaml](https://github.com/XVilka/yara-ocaml)
    - OCaml bindings for YARA
* [yara-parser](https://github.com/Northern-Lights/yara-parser)
    - Tools for parsing rulesets using the exact grammar as YARA. Written in Go.
* [yaraparser](https://github.com/BitsOfBinary/yaraparser)
    - Python 3 tool to parse Yara rules.
* [yaraPCAP](https://github.com/kevthehermit/YaraPcap)
    - YARA scanner For IMAP feeds and saved streams.
* [yara-procdump-python](https://github.com/google/yara-procdump-python)
    - Python extension to wrap the YARA process memory access API.
* [yara-rust](https://github.com/Hugal31/yara-rust)
    - Rust bindings for VirusTotal/Yara
* [yara-signator](https://github.com/fxb-cocacoding/yara-signator) :sparkles:
    - Automatic YARA rule generation for Malpedia
* [YARA-sort](https://github.com/horsicq/YARA-sort)
    - Aggregate files into collections basd on YARA rules. [blog](https://n10info.blogspot.com/2019/10/nfd-sort.html)
* [Yara Python ICAP Server](https://github.com/RamadhanAmizudin/python-icap-yara)
    - ICAP server with YARA scanner.
* [yarasafe](https://github.com/lucamassarelli/yarasafe)
    - Automatic generation of function signature using machine learning.
* [Yara-Scanner](https://github.com/PolitoInc/Yara-Scanner)
    - Python-based extension that integrates a YARA scanner into Burp Suite.
* [yarascanner](https://github.com/jheise/yarascanner)
    - Golang-based web service to scan files with YARA rules.
* [YaraSharp](https://github.com/stellarbear/YaraSharp)
    - C# wrapper around the Yara pattern matching library
* [Yara Toolkit](https://yaratoolkit.securitybreak.io/)
    - This is the Yara editor. You can write your own Yara rules or copy paste one to edit it.
* [YaraStation](https://github.com/NumLocK15/yarastation)
    - Yara station is a managment portal designed to facilitate the use of Loki scanner.
* [yara_tools](https://github.com/matonis/yara_tools)
    - Python bindings to author YARA rules using natural Python conventions.
* [Yara-Validator](https://github.com/CIRCL/yara-validator)
    - Validates YARA rules and tries to repair the broken ones.
* [yaraVT](https://github.com/deadbits/yaraVT)
    - Scan files with Yara and send rule matches to VirusTotal reports as comments.
* [yara_zip_module](https://github.com/stoerchl/yara_zip_module)
    - Search for strings inside a zip file.
* [yarg](https://github.com/immortalp0ny/yarg)
    - IDAPython plugin for gerenating YARA rules from x86/x86-64 code.
* [yarGen](https://github.com/Neo23x0/yarGen)
    - YARA rule generator for finding related samples and hunting.
* [Yara Scanner](https://github.com/ace-ecosystem/yara_scanner)
    - A wrapper around the yara-python project the providing multiple capabilities.
* [Yarasilly2](https://github.com/YARA-Silly-Silly/yarasilly2)
    - A Semi automatic handy tool to generate YARA rules from sample virus files ( WIP ) for Malware Analyst, inspired by DIFF function of VirusTotal Premium Account.
* [yaya](https://github.com/EFForg/yaya)
    - Automatically curate open source yara rules and run scans.
* [YaYaGen](https://github.com/jimmy-sonny/YaYaGen)
    - YARA rule generator for Android malware.
* [Yeti](https://github.com/yeti-platform/yeti)
    - Platform meant to organize observables, indicators of compromise, TTPs, and knowledge on threats in a single, unified repository.
* [yextend](https://github.com/BayshoreNetworks/yextend)
    - YARA integrated software to handle archive file data.
* [yaraZeekAlert](https://github.com/SCILabsMX/yaraZeekAlert) :sparkles:
    - Scans files with YARA rules and send email alerts which include network context of the file transfer and attaches the suspicious file if it is less than 10 MB.
* [yaraScanParser](https://github.com/Sh3llyR/yaraScanParser)
    - Parsing tool for [Yara Scan Service](https://riskmitigation.ch/yara-scan/)'s JSON output file.
* [YARI](https://github.com/avast/yari)
    - Interactive debugger for the YARA language written in Rust.
* [YLS](https://github.com/avast/yls)
    - Language server for YARA to intergrate with e.g. vscode or vim. Offers code completion, function documentation, code formatting, debugging, ...
* [YMCA](https://github.com/m0n4/YARA-Matches-Correspondance-Array)
    - Displays a table of matches between YARA rules and a collection of samples.
* [Yobi](https://github.com/imp0rtp3/Yobi) :sparkles:
    - Yobi is a basic firefox extension which allows to run public or private YARA rules on all scripts and pages rendered by the browser.
* [statiStrings](https://github.com/Sh3llyR/statiStrings)
    - Strings statistics calculator for YARA rules.

## Services

* [Hybrid Analysis YARA Search](https://www.hybrid-analysis.com/yara-search)
    - YARA search / hunting from CrowdStrike / Hybrid Analysis, powered by Falcon MalQuery.
* [InQuest Labs](https://labs.inquest.net) :sparkles: :gem:
    -  See the YARA section for helper routines to convert regular expressions to match on base64 encoded strings, conver strings to sequences of uint() lookups, and more.
* [Koodous](https://koodous.com/)
    - Collaborative platform for APK analysis, with community YARA rule repository and large APK sample dataset.
* [MalShare](https://malshare.com/)
    - Free malware repository providing researchers access to samples, malicous feeds, and YARA results.
* [MalwareConfig](https://malwareconfig.com/)
    - Extract IOCs from Remote Access Trojans.
* [YaraEditor (Web)](https://www.adlice.com/download/yaraeditorweb/)
    - All-in-one website to create and manage YARA rules.
* [YARAify](https://yaraify.abuse.ch/):sparkles:
    - YARAify is a project from abuse.ch that allows anyone to scan suspicious files such as malware samples or process dumps against a large repository of YARA rules.
* [Yara Scan Service](https://riskmitigation.ch/yara-scan/)
    - A simple service to test your Yara rules against a large set of malicious and identified files.

## Syntax Highlighters

* Atom: [language-yara](https://github.com/blacktop/language-yara)
* Emacs: [yara-mode](https://github.com/binjo/yara-mode)
* GTK-based editors, like gedit and xed: [GtkSourceView-YARA](https://github.com/wesinator/GtkSourceView-YARA)
* Notepad++: [userDefinedLanguages](https://github.com/notepad-plus-plus/userDefinedLanguages/blob/master/udl-list.md)
* Sublime Text: [YaraSyntax](https://github.com/nyx0/YaraSyntax/)
* Vim: [vim-yara](https://github.com/yaunj/vim-yara), [vim-syntax-yara](https://github.com/s3rvac/vim-syntax-yara)
* Visual Studio Code: [vscode-yara](https://github.com/infosec-intern/vscode-yara)

## People

We're aggregating the Twitter handles for anyone involved with the projects on this page into a single list: [awesome-yara Twitter list](https://twitter.com/InQuest/lists/awesome-yara). Do let us know if anyone is missing.

## Videos and Talks

* [Finding Evil with YARA](https://www.youtube.com/watch?v=mQ-mqxOfopk)
* [SAS2018: Finding aliens, star weapons and ponies with YARA](https://www.youtube.com/watch?v=fbidgtOXvc0)
* [Costin Raiu - Combining code similarity with Yara to find goodies](https://www.youtube.com/watch?v=DQXpdEvyasc)
* [YARA Rule Processing Sessions - Florian Roth](https://www.youtube.com/playlist?list=PL8OlALxRcWsSEPtN6AujulTHVc9HZMwso)
* [Upping the APT hunting game: learn the best YARA practices from Kaspersky](https://securelist.com/yara-webinar-follow-up/96505/)
* [Star-Gazing | Using a Full Galaxy of YARA Methods to Pursue an Apex Actor | By Greg Lesnewich](https://www.youtube.com/watch?v=aaV7UieJ_l4)
* [Lightweight Binary Similarity - YARA Using PE Features for Quick Wins](https://github.com/g-les/YARA-PE-Features)
* [DEF CON 26 - Andrea Marcelli - Looking for the perfect signature an automatic YARA rules](https://www.youtube.com/watch?v=Dz0C55Azn1Y)

## Related Awesome Lists

* [Crawler](https://github.com/BruceDone/awesome-crawler)
* [CVE PoC](https://github.com/qazbnm456/awesome-cve-poc)
* [Forensics](https://github.com/Cugu/awesome-forensics)
* [Hacking](https://github.com/carpedm20/awesome-hacking)
* [HackwithGithub](https://github.com/Hack-with-Github/Awesome-Hacking)
* [Honeypots](https://github.com/paralax/awesome-honeypots)
* [Incident-Response](https://github.com/meirwah/awesome-incident-response)
* [Infosec](https://github.com/onlurking/awesome-infosec)
* [IOCs](https://github.com/sroberts/awesome-iocs)
* [Malware Analysis](https://github.com/rshipp/awesome-malware-analysis)
* [ML for Cyber Security](https://github.com/jivoi/awesome-ml-for-cybersecurity)
* [OSINT](https://github.com/jivoi/awesome-osint)
* [PCAP Tools](https://github.com/caesar0301/awesome-pcaptools)
* [Pentesting](https://github.com/enaqx/awesome-pentest)
* [Reversing](https://github.com/tylerha97/awesome-reversing)
* [Security](https://github.com/sbilly/awesome-security)
* [Static Analysis](https://github.com/analysis-tools-dev/static-analysis)
* [Threat Detection](https://github.com/0x4D31/awesome-threat-detection)
* [Threat Intelligence](https://github.com/hslatman/awesome-threat-intelligence)

## Contributing

This list is maintained by [InQuest](https://inquest.net/). Feel free to let us
know about anything we're missing!

See [CONTRIBUTING.md](CONTRIBUTING.md).

### Contributors

[![awesome-yara contributors](https://contrib.rocks/image?repo=inquest/awesome-yara&max=100)](https://github.com/inquest/awesome-yara/graphs/contributors)
