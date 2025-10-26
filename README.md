# Home Lab SIEM: Threat Detection with the ELK Stack

## Project Overview

This project involves building a fully functional Security Information and Event Management (SIEM) system from the ground up using the Elastic Stack (ELK: Elasticsearch, Logstash, Kibana). The primary goal is to ingest Windows security logs, parse them for critical security events, create visualizations for monitoring, and develop automated detection rules to identify potential threats.

This lab serves as a hands-on simulation of a real-world security operations center (SOC) environment, demonstrating key cybersecurity skills in log management, threat detection, and incident response.

## Project Objectives

- **Data Ingestion:** Successfully deploy and configure Winlogbeat on a Windows client to forward event logs to a central Logstash instance.
- **Data Parsing & Normalization:** Develop custom Logstash filters to parse raw Windows Event Logs, extracting key fields (e.g., username, source IP, event ID) for effective analysis.
- **Data Storage & Search:** Implement an Elasticsearch cluster to store the parsed logs, enabling fast and efficient searching.
- **Visualization & Monitoring:** Build comprehensive Kibana dashboards to visualize security data, such as failed login attempts and user activity.
- **Threat Detection:** Author and implement detection rules for specific attack patterns, including:
  - Brute Force Attacks
  - (Stretch Goal) Impossible Travel Logins
- **Alerting:** Configure the stack to trigger automated alerts (e.g., via Email) when detection rules are fired.

## Lab Architecture

The following diagram illustrates the data flow and components of this homelab SIEM:

![SIEM Architecture Diagram](images/siem_architecture.png)

### Components

1.  **Windows 10/11 Client VM:** The endpoint generating security logs.
    - **Tool:** Winlogbeat (installed as an agent) to ship logs.
2.  **ELK Server (Ubuntu Server VM):** The central log processing server.
    - **Elasticsearch:** A NoSQL database for storing and indexing logs.
    - **Logstash:** The data processing pipeline that ingests, parses, and enriches logs.
    - **Kibana:** The web interface for searching, visualizing, and managing alerts.
3.  **Virtualization Platform:** VMware Workstation Pro/Fusion or VirtualBox.

## Prerequisites & Tools

- **Virtualization Software:** [VMware Workstation](https://www.vmware.com/products/workstation-pro.html) or [VirtualBox](https://www.virtualbox.org/)
- **Operating Systems:**
  - Ubuntu Server 22.04 LTS (for the ELK Stack)
  - Windows 10/11 (as the log source)
- **Core Stack:**
  - [Elasticsearch 8.x](https://www.elastic.co/elasticsearch/)
  - [Logstash 8.x](https://www.elastic.co/logstash/)
  - [Kibana 8.x](https://www.elastic.co/kibana/)
  - [Winlogbeat 8.x](https://www.elastic.co/beats/winlogbeat)
- **Other Tools:**
  - A text editor (like [VS Code](https://code.visualstudio.com/)) for editing configuration files.
  - [Git](https://git-scm.com/) for version control.

## Project Steps

1.  [Phase 1: Project Setup & Documentation](docs/phase1_setup.md) 
2.  [Phase 2: ELK Stack Deployment](docs/phase2_elk_deployment.md)
3.  [Phase 3: Windows Client Configuration](docs/phase3_win_config.md)
4.  [Phase 4: Logstash Parsing & Pipelines](docs/phase4_logstash_parsing.md)
5.  [Phase 5: Kibana Dashboards & Detection Rules](docs/phase5_kibana_detection.md)

---

## License

This project is for educational purposes.
