OpsPilot exists to proactively detect, report, and automatically recover from common operational failures in cloud-hosted applications, reducing downtime and manual intervention for small engineering teams.



# OpsPilot

**OpsPilot** is a lightweight, cloud-native operations platform designed to monitor application health, analyze system and application logs, alert engineers to emerging issues, and automatically recover from common operational failures.

OpsPilot is intentionally scoped for **small teams and internal platforms** that need reliable operations without a full-time SRE or expensive third-party tooling.

---

#The Problem

Small engineering teams often run production workloads with:
- Limited monitoring
- Incomplete alerting
- Manual log inspection
- Reactive incident response

This leads to:
- Late detection of failures
- Preventable downtime
- Engineers acting as “human monitoring systems”

OpsPilot addresses these gaps by automating observation, notification, and recovery.

---

## What OpsPilot Does

OpsPilot focuses on **three core responsibilities**:

### 1. Monitoring
Continuously observes:
- Application health endpoints
- CPU, memory, and disk usage
- Service uptime
- Error patterns in logs

### 2. Alerting
Notifies engineers via:
- Slack
- Email

Alerts trigger on:
- Resource exhaustion
- Error spikes
- Service restarts
- Failed deployments

### 3. Automated Recovery
Safely handles common failures by:
- Restarting crashed services
- Rotating logs when disk usage is high
- Scaling application workloads when load increases

---

## What OpsPilot Is Not

OpsPilot is **not**:
- A replacement for enterprise monitoring platforms (Datadog, New Relic)
- A business analytics tool
- An AI-based operations product
- A commercial SaaS offering

OpsPilot is an **internal operations platform**, similar to tools built in-house by many engineering teams.

---

##  High-Level Architecture

User
↓
Load Balancer
↓
OpsPilot Web Dashboard (Kubernetes)
↓
Monitoring & Automation Services (Python)
↓
AWS Services (EC2, S3, RDS, CloudWatch)
↓
Alerts (Slack / Email)







Infrastructure is provisioned using Terraform and deployed using Docker and Kubernetes with CI/CD pipelines.

---

## Technology Stack

**Cloud**
- AWS (EC2, S3, RDS, CloudWatch, IAM)

**Infrastructure as Code**
- Terraform

**Containers & Orchestration**
- Docker
- Kubernetes (EKS or local cluster)

**Automation & Backend**
- Python
- Flask / FastAPI
- boto3

**CI/CD**
- GitHub Actions

**Observability**
- Prometheus
- Grafana

**Operating System**
- Linux (hardening, automation, recovery)

---

## Security & Reliability

OpsPilot follows operational best practices:
- Least-privilege IAM
- Encrypted storage
- No hardcoded secrets
- Automated backups
- Documented recovery procedures
- Cost monitoring and cleanup automation

---

##  Failure Scenarios Covered

OpsPilot is designed to detect and respond to:
- Application crashes
- Resource exhaustion (CPU, memory, disk)
- Log file growth
- Failed deployments
- Partial infrastructure failures

Each scenario is documented with detection, alerting, and recovery behavior.

---

##  Why This Project Exists

OpsPilot was built to demonstrate:
- Real-world DevOps decision-making
- Production-minded infrastructure design
- Automation over manual intervention
- Clear documentation and operational discipline

This project reflects how modern DevOps engineers design, deploy, monitor, and maintain systems—not just how they provision infrastructure.

---

## Documentation

- Architecture diagrams: `/diagrams`
- Infrastructure code: `/terraform`
- Kubernetes manifests: `/k8s`
- Automation scripts: `/automation`
- CI/CD pipelines: `/ci`
- Learning and incident logs: `/learning-log.md`

---

## Author

Built as a hands-on DevOps engineering project focused on real operational problems, reliability, and maintainability.

---

## 📝 License

MIT License
