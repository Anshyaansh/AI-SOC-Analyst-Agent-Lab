# 🛡️ AI-Powered SOC Analyst Automation Lab

An automated Tier-1 Security Operations Center (SOC) home lab. This project captures live network traffic, uses dynamic thresholds to identify malicious activity across multiple protocols (ICMP, SSH), and leverages an LLM-powered AI agent to generate structured triage reports.

---

## 🏗️ Architecture 

* **Attacker (Threat Actor):** Ubuntu Server generating malicious traffic.
* **Defender (SOC Target):** Kali Linux running the automated Python capture script.
* **AI Engine:** Airia.ai running a custom GPT-5 Nano agent programmed with a strict defensive SOC playbook.

---

## ⚙️ Configuration

To run this in your own environment, update the `CONFIGURATION` section in `soc_capture.py`:

```python
# Network Variables
INTERFACE = "eth0"              
DESTINATION_IP = "192.168.56.20" 

# Airia API Credentials
AIRIA_API_URL = "YOUR_EXECUTION_URL"
AIRIA_API_KEY = "YOUR_API_KEY"
