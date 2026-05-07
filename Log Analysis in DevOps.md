# Log Analysis in DevOps

## What is Log Analysis?

Log analysis is the process of:
- Collecting logs
- Monitoring logs
- Analyzing logs
- Detecting issues from logs

Logs help DevOps engineers:
- Debug errors
- Monitor systems
- Detect failures
- Improve performance
- Ensure security

---

# Why Log Analysis is Important?

Without logs:
- Hard to identify issues
- Difficult troubleshooting
- No visibility into systems

Log analysis helps:
- Detect failures quickly
- Monitor infrastructure
- Improve application reliability

---

# Types of Logs

| Log Type | Description |
|---|---|
| Application Logs | Application events/errors |
| System Logs | OS-related logs |
| Server Logs | Web server logs |
| Security Logs | Authentication/security events |
| Container Logs | Docker/Kubernetes logs |
| CI/CD Logs | Jenkins/GitHub Actions logs |

---

# Linux Log Analysis

---

# Important Linux Log Files

| File | Purpose |
|---|---|
| /var/log/syslog | System logs |
| /var/log/auth.log | Authentication logs |
| /var/log/kern.log | Kernel logs |
| /var/log/dmesg | Boot logs |
| /var/log/nginx/access.log | Nginx access logs |
| /var/log/nginx/error.log | Nginx error logs |

---

# Linux Log Commands

---

# View Logs

```bash
cat /var/log/syslog
```

---

# View Large Logs

```bash
less /var/log/syslog
```

---

# Real-Time Log Monitoring

```bash
tail -f /var/log/syslog
```

---

# Last 100 Lines

```bash
tail -100 /var/log/syslog
```

---

# Search Errors

```bash
grep "error" /var/log/syslog
```

---

# Search Multiple Keywords

```bash
grep -Ei "error|failed|warning" logfile.log
```

---

# Count Matching Lines

```bash
grep -c "error" logfile.log
```

---

# Docker Log Analysis

---

# View Container Logs

```bash
docker logs container_id
```

---

# Follow Real-Time Logs

```bash
docker logs -f container_id
```

---

# Last 50 Log Lines

```bash
docker logs --tail 50 container_id
```

---

# Docker Compose Logs

```bash
docker-compose logs
```

---

# Real-Time Docker Compose Logs

```bash
docker-compose logs -f
```

---

# Kubernetes Log Analysis

---

# View Pod Logs

```bash
kubectl logs pod_name
```

---

# Follow Real-Time Pod Logs

```bash
kubectl logs -f pod_name
```

---

# Logs for Specific Container

```bash
kubectl logs pod_name -c container_name
```

---

# Previous Container Logs

```bash
kubectl logs pod_name --previous
```

---

# View All Pods

```bash
kubectl get pods
```

---

# Describe Pod

```bash
kubectl describe pod pod_name
```

Useful for:
- CrashLoopBackOff
- Failed scheduling
- Resource issues

---

# Jenkins Log Analysis

---

# Jenkins Service Logs

```bash
sudo journalctl -u jenkins
```

---

# Real-Time Jenkins Logs

```bash
sudo journalctl -u jenkins -f
```

---

# Jenkins Console Logs

Inside Jenkins:
```text
Job → Console Output
```

Used for:
- Build failures
- Deployment issues
- Pipeline debugging

---

# Common Jenkins Errors

| Error | Meaning |
|---|---|
| Build Failed | Compilation/Test failure |
| Permission Denied | Access issue |
| Docker Not Found | Docker missing |
| Port Conflict | Port already used |

---

# GitHub Actions Log Analysis

---

# Workflow Logs

GitHub:
```text
Repository → Actions → Workflow Run
```

Used for:
- CI/CD debugging
- Build failures
- Deployment errors

---

# AWS Log Analysis

---

# EC2 Logs

```bash
sudo journalctl
```

---

# CloudWatch Logs

AWS service for:
- Log monitoring
- Alerts
- Metrics
- Real-time analysis

---

# View CloudWatch Logs

AWS Console:
```text
CloudWatch → Logs
```

---

# Nginx Log Analysis

---

# Access Logs

```bash
cat /var/log/nginx/access.log
```

---

# Error Logs

```bash
cat /var/log/nginx/error.log
```

---

# Search 404 Errors

```bash
grep "404" /var/log/nginx/access.log
```

---

# Apache Log Analysis

---

# Apache Access Logs

```bash
cat /var/log/apache2/access.log
```

---

# Apache Error Logs

```bash
cat /var/log/apache2/error.log
```

---

# Monitoring & Logging Tools

| Tool | Purpose |
|---|---|
| ELK Stack | Centralized logging |
| Prometheus | Monitoring |
| Grafana | Visualization |
| Loki | Log aggregation |
| Splunk | Enterprise log analysis |
| Fluentd | Log collection |
| Graylog | Log management |

---

# ELK Stack

ELK:
- Elasticsearch
- Logstash
- Kibana

Used for:
- Centralized log analysis
- Searching logs
- Visualizing logs

---

# ELK Workflow

```text
Applications
      ↓
Logstash
      ↓
Elasticsearch
      ↓
Kibana Dashboard
```

---

# Prometheus + Grafana

Used for:
- Monitoring
- Metrics visualization
- Alerting

---

# Loki + Grafana

Loki collects logs.

Grafana visualizes logs.

---

# Common Log Analysis Tasks

| Task | Purpose |
|---|---|
| Error Detection | Find failures |
| Performance Monitoring | Detect slow systems |
| Security Monitoring | Detect attacks |
| Troubleshooting | Debug issues |
| Audit Tracking | Track activities |

---

# Important Log Analysis Commands

| Command | Purpose |
|---|---|
| tail -f | Real-time logs |
| grep | Search logs |
| less | Read large logs |
| journalctl | Systemd logs |
| docker logs | Container logs |
| kubectl logs | Kubernetes logs |

---

# Best Practices

- Centralize logs
- Rotate logs regularly
- Monitor logs continuously
- Create alerts
- Secure sensitive logs

---

# Log Rotation

Prevent logs from filling storage.

Linux tool:
```bash
logrotate
```

---

# Real-World DevOps Log Workflow

```text
Application Running
        ↓
Generate Logs
        ↓
Collect Logs
        ↓
Store Centrally
        ↓
Analyze Logs
        ↓
Create Alerts
```

---

# Advantages of Log Analysis

- Faster troubleshooting
- Better monitoring
- Improved security
- Performance optimization
- High system reliability

---

# Learning Outcome

After learning log analysis:
- You can troubleshoot systems
- Debug DevOps pipelines
- Monitor applications
- Detect failures quickly

---

# Recommended Next Topics

After log analysis learn:
1. Monitoring
2. Prometheus
3. Grafana
4. ELK Stack
5. Kubernetes Monitoring
6. DevSecOps

---

# Author

## Gourav Lande

Interested in:
- DevOps
- Cloud Computing
- AI Engineering
- MLOps

GitHub:
https://github.com/gouravlande

---

# Conclusion

Log analysis is one of the most important skills in DevOps. It helps engineers monitor systems, debug failures, improve reliability, and maintain production environments efficiently.
