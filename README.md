# KubeLab — Kubernetes Practice Lab

> **Live site:** [kubelab.eknathalabs.com](https://kubelab.eknathalabs.com)  
> Built by [Eknatha Reddy Puli](https://eknathalabs.com) · Platform Engineer  

A structured, hands-on Kubernetes learning lab — 12 learning modules, 9 fully offline interactive tools, a 200+ command cheatsheet, a 100-question CKA/CKS quiz, 12 practice labs, and a 60+ error encyclopedia. Built by a Platform Engineer, for Platform Engineers.

---

## What's Inside

| Section | Count | Description |
|---|---|---|
| Learning Modules | 12 | Structured deep-dives from cluster architecture to GKE |
| Offline Tools | 9 | YAML generator, troubleshooter, RBAC, PromQL, Helm, and more |
| kubectl Cheatsheet | 200+ | Searchable, click-to-copy commands with CKA shortcuts |
| CKA/CKS Quiz | 100 | Scenario-based questions, filterable by topic and difficulty |
| Practice Labs | 12 | Step-by-step walkthroughs from Beginner to CKS-level Advanced |
| Error Encyclopedia | 60+ | K8s errors — root cause, fix commands, and prevention |

---

## Pages

### Modules
12 structured learning modules covering the full Kubernetes landscape. Each module includes an overview, key concept cards, essential commands, a YAML example, and study resources. Filterable by level (Beginner / Intermediate / Advanced / CKA / CKS).

| # | Module | Level |
|---|---|---|
| 01 | Cluster Architecture | Beginner |
| 02 | Pods & Workloads | Beginner |
| 03 | Networking | Intermediate |
| 04 | Storage & Volumes | Intermediate |
| 05 | RBAC & Security | Intermediate |
| 06 | Config & Secrets | Beginner |
| 07 | Scaling & Scheduling | Intermediate |
| 08 | Observability | Intermediate |
| 09 | Helm & GitOps | Intermediate |
| 10 | Troubleshooting | Advanced |
| 11 | CKS Advanced Security | Advanced |
| 12 | GKE & Cloud K8s | Advanced |

### Tools — 100% Offline
All 9 tools run entirely in the browser. No API keys, no network requests, no external dependencies.

| Tool | What it does |
|---|---|
| ⚡ YAML File Generator | Select resource kind + fill fields → complete, annotated manifest for 14 resource types |
| 🔍 K8s Troubleshooter | Paste `kubectl` output or logs → pattern-matched root cause, fix commands, prevention |
| 📄 YAML Validator & Explainer | Paste any manifest → field-by-field explanation, detected issues, improvement suggestions |
| 🔒 Network Policy Builder | Choose namespaces + policy type → production-ready `NetworkPolicy` YAML |
| ⛑️ RBAC Generator | Pick resources + verbs + scope → `ServiceAccount` + `Role` + `RoleBinding` YAML |
| 📊 PromQL Query Builder | Choose metric category + namespace → 3 ready-to-use queries + `PrometheusRule` alert YAML |
| 🪖 Helm Values Generator | Pick chart + environment → production-grade `values.yaml` (8 charts supported) |
| 📐 Resource Calculator | App type + RPS + replicas → computed requests/limits YAML + HPA config |
| 🐳 Dockerfile Linter | Paste Dockerfile → security issues, optimization tips, improved Dockerfile template |

**YAML File Generator** supports 14 resource kinds:
`Deployment`, `StatefulSet`, `DaemonSet`, `Job`, `CronJob`, `Service`, `Ingress`, `ConfigMap`, `Secret`, `PersistentVolumeClaim`, `HorizontalPodAutoscaler`, `NetworkPolicy`, `ServiceAccount`, `Namespace`

**PromQL Builder** covers 8 metric categories:
CPU, Memory, Pod restarts, Network traffic, Storage/PVC, HTTP latency, HTTP error rate, Node health

**Helm Values Generator** supports 8 charts:
`ingress-nginx`, `postgresql`, `redis`, `kafka`, `kube-prometheus-stack`, `cert-manager`, `argo-cd`, generic app

### Cheatsheet
200+ `kubectl` commands across 10 categories — searchable by keyword, click any command to copy to clipboard. CKA exam shortcuts included.

Categories: Pods & Workloads · Deployments & Rollouts · Debugging · Networking · Storage · RBAC & Security · Namespaces & Context · Helm · etcd & Control Plane · CKA Exam Shortcuts

### Quiz
100 scenario-based questions covering CKA and CKS exam domains. Features live score tracking, a progress bar, and per-question explanations.

- Filter by topic: Architecture · Networking · Storage · Security / RBAC · Workloads · Scheduling · Observability · Helm / GitOps · Troubleshooting · CKS Advanced
- Filter by difficulty: Easy · Medium · Hard

### Labs
12 full step-by-step lab walkthroughs modelled on production incidents and CKA/CKS exam tasks. Each lab lists prerequisites, numbered steps with copy-ready commands, and a cleanup section.

| Difficulty | Labs |
|---|---|
| Beginner | Pod Scheduling Debug, ConfigMap & Secret Injection, Rolling Update & Rollback |
| Intermediate | PVC Binding & Storage Debugging, NetworkPolicy Enforcement, HPA Load Testing, RBAC Least Privilege |
| Advanced | CKS Runtime Security with Falco, etcd Backup & Restore, Multi-tenancy with Namespaces & Quotas, GitOps with ArgoCD, TLS Certificate Rotation |

### Error Encyclopedia
60+ Kubernetes errors categorised by severity (Critical / Warning / Info) and type. Click any error to expand root cause, diagnosis steps, fix commands (click to copy), and prevention advice.

Categories: Pod Status · Scheduling · Networking · Storage · RBAC · Cluster · Helm

Common errors covered: `OOMKilled` · `CrashLoopBackOff` · `ImagePullBackOff` · `Pending` · `Evicted` · `CreateContainerConfigError` · `Terminating` (stuck) · `ErrImageNeverPull` · `FailedMount` · `Forbidden` · `certificate has expired` · Helm install/upgrade failures · and many more.

---

## Tech Stack

- **Pure HTML/CSS/JavaScript** — single `index.html`, zero build step, zero dependencies
- **No backend** — everything runs client-side
- **No API keys** — all tools are offline-first; removed all external AI API calls
- **Fonts** — JetBrains Mono · Syne · Inter (Google Fonts)
- **Hosting** — static file, deployable anywhere (Netlify, GitHub Pages, S3, nginx)

---

## Offline Tools — Implementation Notes

All tools were converted from AI API calls to pure client-side logic:

- **Troubleshooter** — regex pattern matching against 10 common K8s error signatures
- **YAML Explainer** — line-by-line YAML parsing, field lookup table, static issue detection rules
- **Network Policy Builder** — parameterised YAML templates for 4 policy types
- **RBAC Generator** — checkbox-driven resource/verb matrix → Role + RoleBinding scaffolding
- **PromQL Builder** — 8 metric category templates × time window × namespace filter
- **Helm Values Generator** — per-chart templates tuned for dev / staging / production
- **Resource Calculator** — empirical per-app-type baseline profiles + RPS/replica math
- **Dockerfile Linter** — static analysis rules checking for ~12 common issues + template improved Dockerfile
- **YAML Generator** — 14 resource kind templates with optional probes, securityContext, HPA, PDB

---

## Related Projects

- [eknathalabs.com](https://eknathalabs.com) — main blog and engineering notes
- [linux.eknathalabs.com](https://linux.eknathalabs.com) — Linux practice lab *(coming soon)*
- [terraform.eknathalabs.com](https://terraform.eknathalabs.com) — Terraform practice lab *(coming soon)*

---

## License

MIT — free to use, fork, and adapt. Attribution appreciated.

---

*Built with ☕ by [EknathaLabs](https://eknathalabs.com)*
