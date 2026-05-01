# KubeLab — Kubernetes Practice Lab

> **kubelab.eknathalabs.com** · Built by [Eknatha Reddy Puli](https://eknathalabs.com) · Free forever · No signup required

A structured, hands-on Kubernetes learning lab covering concepts, interactive AI-powered tools, a 200+ command cheatsheet, a 100-question CKA/CKS quiz, and full lab walkthroughs — all in a single `index.html` file.

---

## 🚀 Live Site

**[kubelab.eknathalabs.com](https://kubelab.eknathalabs.com)**

Part of the **eknathalabs.com** ecosystem:

| Subdomain | Topic |
|---|---|
| [kubelab.eknathalabs.com](https://kubelab.eknathalabs.com) | Kubernetes |
| [linux.eknathalabs.com](https://linux.eknathalabs.com) | Linux for DevOps |
| [terraform.eknathalabs.com](https://terraform.eknathalabs.com) | Terraform / IaC |
| [eknathalabs.com](https://eknathalabs.com) | Home · All Labs |

---

## 📦 What's Inside

### 📚 12 Learning Modules

Structured from beginner to CKS-level advanced. Each module opens a full detail view with overview, key concepts, essential commands, YAML examples, and study resources.

| # | Module | Level | Tags |
|---|---|---|---|
| 01 | Cluster Architecture | Beginner | CKA |
| 02 | Pods & Workloads | Beginner | CKA |
| 03 | Networking | Intermediate | CKA · CKS |
| 04 | Storage & Volumes | Intermediate | CKA |
| 05 | RBAC & Security | Intermediate | CKA · CKS |
| 06 | Config & Secrets | Beginner | CKA |
| 07 | Scaling & Scheduling | Intermediate | CKA |
| 08 | Observability | Intermediate | CKA |
| 09 | Helm & Package Mgmt | Intermediate | CKA |
| 10 | GitOps & ArgoCD | Advanced | CKS |
| 11 | CKS Security Deep Dive | Advanced | CKS |
| 12 | GKE & Cloud Kubernetes | Advanced | CKS |

Filter modules by: **All · Beginner · Intermediate · Advanced · CKA · CKS**

---

### 🤖 8 AI-Powered Tools

All tools are powered by the Claude API — paste input, get instant expert output.

| Tool | What it does |
|---|---|
| **K8s Troubleshooter** | Paste pod logs / kubectl output → RCA + fix commands |
| **YAML Validator & Explainer** | Paste K8s manifest → field-by-field explanation + issues flagged |
| **Network Policy Builder** | Define ingress/egress rules → production-ready NetworkPolicy YAML |
| **RBAC Generator** | Describe what an SA needs → Role + RoleBinding YAML |
| **PromQL Query Builder** | Describe what to monitor → PromQL expression + alert rule |
| **Helm Values Generator** | Chart + environment → commented values.yaml |
| **Resource Calculator** | App type + RPS → CPU/memory requests, limits, HPA config |
| **Dockerfile Linter** | Paste Dockerfile → security issues + optimized rewrite |

---

### ⌘ kubectl Cheatsheet

200+ commands across 12 categories. **Searchable** — type to filter. **Click any command to copy** to clipboard.

Categories: Pods & Workloads · Deployments & Rollouts · Debugging · Networking · Storage · RBAC & Security · Config & Secrets · Namespaces & Context · CKA Exam Tips · HPA & Scaling · Helm · ArgoCD & GitOps

---

### ✦ 100-Question CKA / CKS Quiz

Scenario-based questions modelled on real exam patterns. Filter by topic and difficulty. Tracks score with a progress bar and grades you at the end.

**Topics (10 questions each):**

- Architecture
- Networking
- Storage
- Security / RBAC
- Workloads
- Scheduling
- Observability
- Helm / GitOps
- Troubleshooting
- CKS Advanced

**Difficulty levels:** Easy · Medium · Hard

Every question includes a detailed explanation shown after answering.

---

### ⚗ 12 Practice Labs

Full step-by-step lab walkthroughs with commands ready to copy, prerequisites, verification steps, and cleanup commands.

| # | Lab | Difficulty | Time |
|---|---|---|---|
| 01 | Deploy a Multi-tier App with Services and Ingress | Beginner | 30 min |
| 02 | Debug a CrashLoopBackOff Pod — OOMKilled | Beginner | 20 min |
| 03 | Work with ConfigMaps and Secrets | Beginner | 25 min |
| 04 | Configure RBAC for a CI/CD Service Account | Intermediate | 30 min |
| 05 | Set Up Horizontal Pod Autoscaler | Intermediate | 35 min |
| 06 | Implement Network Policies for Namespace Isolation | Intermediate | 40 min |
| 07 | StatefulSet with PersistentVolume | Intermediate | 35 min |
| 08 | Deploy ArgoCD and Set Up GitOps | Advanced | 60 min |
| 09 | etcd Backup and Restore | Advanced | 35 min |
| 10 | Secure a Cluster with OPA Gatekeeper | Advanced | 50 min |
| 11 | Falco Runtime Security Monitoring | Advanced | 45 min |
| 12 | GKE Workload Identity Setup | Advanced | 40 min |

---


## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML · CSS · Vanilla JavaScript |
| AI Tools | Claude API (`claude-sonnet-4-20250514`) |
| Fonts | JetBrains Mono · Syne · Inter (Google Fonts) |
| Hosting | GitHub Pages |
| Build | None — zero build step |

---

## ⚙️ Configuration

The AI tools call the Claude API directly from the browser. No API key setup is required when running on **claude.ai** — the API key is handled by the platform.

If self-hosting outside Claude's environment, add your API key:

```javascript
// In the fetch() call inside runTool():
headers: {
  'Content-Type': 'application/json',
  'x-api-key': 'YOUR_ANTHROPIC_API_KEY',    // add this
  'anthropic-version': '2023-06-01',          // add this
  'anthropic-dangerous-direct-browser-calls': 'true'  // required for browser
}
```

> ⚠️ Never commit API keys to a public repository. Use environment variables or a backend proxy for production.

---

## 🗺 Roadmap

- [ ] More quiz questions (target: 200)
- [ ] Progress tracking with localStorage
- [ ] Module completion checkmarks
- [ ] Printable cheatsheet PDF export
- [ ] Dark/light theme toggle
- [ ] CKS-specific lab track
- [ ] Community submissions via GitHub Issues

---

## 🤝 Contributing

Contributions are welcome — especially new quiz questions, lab scenarios, and cheatsheet commands.

1. Fork the repository
2. Add your content to the relevant data array in `index.html` (`QUIZ_BANK`, `LABS`, `CHEATSHEET`, `MODULES`)
3. Test locally
4. Open a Pull Request with a description of what you added

For bug reports or feature requests, open a [GitHub Issue](https://github.com/eknathareddyp/kubelab/issues).

---

## 👤 Author

**Eknatha Reddy Puli** 

- 🌐 [eknathalabs.com](https://eknathalabs.com)
- 💼 [LinkedIn](https://linkedin.com/in/eknathareddyp)
- 🐙 [GitHub @eknathareddyp](https://github.com/eknathareddyp)
- 🎓 CKA · CKS (in progress) · Terraform Associate (in progress)

---

## 📄 License

MIT License — free to use, modify, and distribute with attribution.

---

*Built with ❤️ for the Kubernetes and DevOps community · Part of [eknathalabs.com](https://eknathalabs.com)*
