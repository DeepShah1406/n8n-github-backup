# n8n Workflows Repository

[![n8n](https://img.shields.io/badge/n8n-v1.121.3-blue)](https://n8n.io)
[![Docker](https://img.shields.io/badge/Docker-v4.54.0-blue)](https://www.docker.com/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)
[![GitHub](https://img.shields.io/badge/GitHub-Backup%20System-informational)](https://github.com)

A collection of **n8n workflows** automatically backed up to GitHub. These workflows run on a local n8n instance (Docker) and are synced daily to this repository.

## 📁 Repository Structure

```
n8n-backup-demo/
├── README.md                      # This file
└── workflows/                     # All n8n workflows
    ├── README.md                  # Workflow descriptions
    └── [workflow-id].json         # Individual workflow files
```

## 🔄 Automatic Backup System

This repository uses an **automated n8n workflow** that:
- Runs on a **daily schedule** (configurable)
- Fetches all workflows from the local n8n instance
- Detects changes (new, modified, or unchanged)
- Pushes updates to GitHub with descriptive commit messages

**Result**: No more manual backups! All workflows are automatically synced instead of doing it 2-3 times per day manually.

## 📝 Workflows

See [workflows/README.md](workflows/README.md) for a detailed description of each workflow.

## 🚀 Quick Setup (If Using This Repository)

1. **Create GitHub Personal Access Token**
   - Go to GitHub → Settings → Developer settings → Personal access tokens
   - Generate token with `repo` scope
   
2. **Configure n8n Credentials**
   - Add GitHub credential with your PAT
   - Add n8n API credential

3. **Import Backup Workflow**
   - Import `VDprFSSHtBm90rYW.json` (simple) or `svFaEYoxV2CylbRb.json` (tag-based)
   - Edit the **Globals** node with your GitHub username, repo name, and path

4. **Activate & Schedule**
   - Enable the workflow
   - Configure the schedule trigger (default: daily)
   - Or trigger manually from n8n UI

## ⚙️ Configuration

Edit the **Globals** node in the backup workflow:

```json
{
  "repo": {
    "owner": "YOUR_GITHUB_USERNAME",
    "name": "YOUR_REPO_NAME",
    "path": "workflows/"
  }
}
```
---

## Contact

- 📧 Email: [shahdeep1406@gmail.com](mailto:shahdeep1406@gmail.com)
- 🐙 GitHub: [DeepShah1406](https://github.com/DeepShah1406)
- 💼 LinkedIn: [deepshah1406](https://www.linkedin.com/in/deepshah1406)
- 🌐 Website: [Deep Shah](https://deepshah1406.github.io/)

---

**Last Updated**: December 2025