<h1 align="center">🎬 Netflix Clone — Enterprise DevOps CI/CD Project</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Cloud-AWS-orange?logo=amazonaws" />
  <img src="https://img.shields.io/badge/CI/CD-Jenkins-blue?logo=jenkins" />
  <img src="https://img.shields.io/badge/Monitoring-Prometheus+Grafana-orange?logo=grafana" />
  <img src="https://img.shields.io/badge/Security-Trivy+OWASP-red?logo=owasp)"/>
  <img src="https://img.shields.io/badge/Kubernetes-EKS+ArgoCD-blue?logo=kubernetes" />
  <img src="https://img.shields.io/badge/License-MIT-green?logo=open-source-initiative" />
</p>

<hr />

<h2>🚀 Overview</h2>

<p>This project implements a full-scale <strong>DevOps pipeline</strong> to deploy a <strong>Netflix Clone App</strong> using industry best practices. It integrates:</p>

<p>✅ CI/CD | ✅ Security | ✅ Containerization | ✅ GitOps | ✅ Monitoring | ✅ Cloud Native Deployment</p>

<hr />

<h2>🛠 Tools Overview</h2>

<p align="center">
  <img src="assets/Devsecops tools.png" alt="Tools Used" width="80%" />
</p>

<hr />

<h2>🧰 Tech Stack &amp; Tools Used</h2>

<p>| Domain | Tools |
|--------|-------|
| ☁️ <strong>Cloud</strong> | <img src="https://img.shields.io/badge/AWS-EC2%20%7C%20EKS-orange?logo=amazonaws" alt="AWS" title="" /> |
| 🔧 <strong>CI/CD</strong> | <img src="https://img.shields.io/badge/Jenkins-Automation-blue?logo=jenkins" alt="Jenkins" title="" /> |
| 🛡 <strong>Security Scanning</strong> | <img src="https://img.shields.io/badge/SonarQube-Code%20Quality-blue?logo=sonarqube" alt="SonarQube" title="" /> <img src="https://img.shields.io/badge/Trivy-Vulnerability-red?logo=aqua" alt="Trivy" title="" /> <img src="https://img.shields.io/badge/OWASP-Dependency--Check-critical?logo=owasp" alt="OWASP" title="" /> |
| 🐳 <strong>Containers</strong> | <img src="https://img.shields.io/badge/Docker-Containerization-blue?logo=docker" alt="Docker" title="" /> |
| 📊 <strong>Monitoring</strong> | <img src="https://img.shields.io/badge/Prometheus-Metrics-orange?logo=prometheus" alt="Prometheus" title="" /> <img src="https://img.shields.io/badge/Grafana-Dashboards-yellow?logo=grafana" alt="Grafana" title="" /> <img src="https://img.shields.io/badge/Node%20Exporter-Server%20Metrics-brightgreen?logo=linux" alt="Node Exporter" title="" /> |
| 🚀 <strong>GitOps</strong> | <img src="https://img.shields.io/badge/Argo%20CD-Kubernetes%20Deployments-blue?logo=argo" alt="ArgoCD" title="" /> |
| 📦 <strong>Version Control</strong> | <img src="https://img.shields.io/badge/GitHub-Code%20Hosting-black?logo=github" alt="GitHub" title="" /> |</p>

<hr />

<h2>🧩 Architecture Diagram</h2>

<p align="center">
  <img src="assets/DevSecOps Architecture.png" alt="Architecture Diagram" width="90%" />
</p>

<hr />

<h2>🧪 Pipeline Workflow</h2>

<h3>🔹 Phase 1: CI/CD via EC2</h3>

<ol>
<li>👨‍💻 Developer pushes code to GitHub.</li>
<li>🤖 Jenkins:
<ul><li>Checks out code</li>
<li>Runs <strong>SonarQube</strong>, <strong>Trivy</strong>, and <strong>OWASP Dependency-Check</strong></li>
<li>Builds app with Node.js</li>
<li>Builds Docker image</li>
<li>Pushes to container registry</li>
<li>Deploys on EC2 Docker container</li></ul></li>
<li>📈 Monitoring Setup:
<ul><li><strong>Node Exporter</strong> + <strong>Prometheus</strong> + <strong>Grafana</strong></li></ul></li>
<li>🌐 EC2 has an <strong>Elastic IP</strong> for public access.</li>
</ol>

<hr />

<h3>🔹 Phase 2: GitOps Deployment to Kubernetes via Argo CD</h3>

<ol>
<li>☁️ AWS EKS cluster provisioned</li>
<li>📦 Argo CD installed inside the cluster</li>
<li>🔁 Argo CD:
<ul><li>Monitors GitHub for K8s manifests</li>
<li>Deploys latest Docker image to EKS</li></ul></li>
<li>🎯 Kubernetes-native Netflix Clone running on EKS!</li>
</ol>

<hr />

<h2>📁 Project Structure</h2>

<p>```bash
.
├── assets/
│   ├── tools.png
│   └── architecture.png
├── Jenkinsfile
├── Dockerfile
├── deployment/
│   └── k8s-manifests/
├── monitoring/
│   ├── prometheus.yml
│   └── grafana-dashboards/
├── owasp-report/
├── trivy-report/
├── src/
├── README.md</p>

