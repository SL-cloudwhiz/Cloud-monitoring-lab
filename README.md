# Cloud Monitoring & Incident Response Lab

A hands-on CloudOps project built to demonstrate real-world monitoring, logging, alerting, and incident response in AWS using an EC2 instance, Nginx, CloudWatch Agent, dashboards, and alerts.

For the full demo + screenshots + incident breakdown → visit my portfolio:

👉 **Portfolio Project Page:** 
👉 **Demo Video:** 

---

## 🔧 Tools & Services
- Amazon EC2
- Amazon CloudWatch (Metrics, Logs, Dashboards, Alarms)
- Nginx Web Server
- CloudWatch Agent
- Bash + stress tool

---

## 🚀 What You Will See in the Demo
- CPU spike simulation using `stress`
- Disk usage spike
- Nginx outage simulation
- Noisy alert → tuned alert comparison
- Custom dashboard with CPU, memory, disk, request rate
- Metric filters for log-based metrics (RequestCount)
- Runbook-style incident response

---

## 📦 Setup Summary
```bash
# Install nginx
sudo yum install -y nginx
sudo systemctl start nginx

# Install CloudWatch agent
sudo yum install -y amazon-cloudwatch-agent

# Trigger CPU spike
stress --cpu 4 --timeout 120

# Trigger disk spike
dd if=/dev/zero of=/var/diskfill.img bs=1M count=500

# Stop nginx
sudo systemctl stop nginx


