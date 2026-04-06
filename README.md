# Linux Security Baseline & Audit Tool

### Objective
An automated shell script designed to perform **rapid telemetry collection** and **security posture assessment** for RHEL-based Linux distributions. This tool is intended for use by Platform Engineers and Security Analysts to establish a "known-good" baseline before pentesting or hardening activities.

### Key Audit Points:
* **Identity & Access:** Extracts active shell users and credential locations.
* **Network Security:** Audits `iptables` rules, `firewalld` configurations, and active interfaces.
* **Compliance:** Checks **SELinux status** and OS/Kernel versioning for vulnerability mapping.
* **Service Hygiene:** Lists all active vs. inactive services to identify "shadow" applications.

### How to Run:
```bash
chmod +x script.sh
sudo ./script.sh > audit_report_$(date +%F).txt
