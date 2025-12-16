# n8n Workflows Directory

[![n8n](https://img.shields.io/badge/n8n_v1.121.3-Automation-blue)](https://n8n.io)
[![Docker](https://img.shields.io/badge/Docker_v4.54.0-Supported-2496ED)](https://www.docker.com)

Complete collection of n8n automation workflows for content creation, data processing, news aggregation, and AI-powered automation tasks.

---

## 📋 Workflows Overview

### 🔄 System & Automation

| Workflow | ID | Purpose |
|----------|----|----|
| **Backup your workflows to GitHub** | `VDprFSSHtBm90rYW` | Automatically backs up all workflows to a GitHub repository in a flat structure |
| **Backup your workflows to GitHub -- in (subfolders)** | `svFaEYoxV2CylbRb` | Backs up all workflows organized by tags into GitHub subfolders |
| **Auto fill data generator** | `4OXebrGzNcxoG2xf` | Generates and auto-fills data for various automation tasks |
| **Auto_fill_Rephrase_Assistant_29_11_2025** | `TNOomDKq6CsVjMaS` | AI-powered assistant for auto-filling and rephrasing content |
| **Auto_fill_Multiple_Rephrase_Assistant_03_12_2025** | `rUs6Rk6EvsYlypmD` | Advanced rephrase assistant supporting multiple content variations |

### 📰 News & Content Aggregation

| Workflow | ID | Purpose |
|----------|----|----|
| **News Workflow 2.0** | `OgVLiE0gHzvIKkiZ` | Main news aggregation and processing workflow |
| **News Workflow 2.0 Big list** | `dXMLuhJuh7ujLMo5` | Aggregates news from large source list |
| **News Workflow 2.0 Google list** | `LIxtfKyl7NPv3e0T` | Aggregates news using Google as source |
| **News Workflow 2.0 XDA List** | `LTQ71uW4jdYbyBpf` | Tech news from XDA and similar sources |
| **News Workflow 1.9** | `Ibp2QFwpZaIBs3IU` | Legacy news workflow (previous version) |
| **News Workflow 1.9** | `saJokXDSlWpMgU3W` | Duplicate news workflow for redundancy |
| **Hacker_News** | `3iSfxi3LCC4jNBmj` | Scrapes and processes Hacker News stories |
| **Create an RSS feed based on a website's content** | `pG4rtJTs0sYUQPDI` | Converts website content into RSS feed format |
| **RSS Feed Scraper - YT** | `w1Koj8H9T2Bv0L5B` | Scrapes RSS feeds from YouTube channels |

### 🤖 AI & Content Generation

| Workflow | ID | Purpose |
|----------|----|----|
| **Generate UGCs using AI** | `VMTmLCkjg4tDeb3E` | AI-powered generation of user-generated content (UGCs) |
| **Rephrase Assistant** | `9Qp6sMw7Oh9ZQAsD` | AI assistant for rephrasing and rewriting content |
| **Email Triage Agent (with Gmail)** | `qKCKxLVnfHPcVgel` | AI agent for classifying and triaging emails using Gmail integration |
| **vector_store_workflow** | `WO3yYI2DnUv5dw5x` | Vector database and embedding management workflow |
| **vector_store_workflow copy** | `dJPdAirFNZXmJ5TT` | Duplicate vector store workflow |

### 📱 Social Media & Scraping

| Workflow | ID | Purpose |
|----------|----|----|
| **Instagram Analytics to Optimized Schedule** | `6xIqBKsyDhY1enSM` | Analyzes Instagram analytics and generates optimal posting schedule |
| **Instagram Analytics to Optimized Schedule using llm** | `0ojGCN2R8r9Ngnnn` | AI-enhanced Instagram scheduling using LLM |
| **Insta_Scraper** | `Jp2cUpMybhrb4jDJ` | Scrapes Instagram data and content |
| **linkedin_Scraper** | `jGcbY3QoynL1Y4xZ` | Scrapes LinkedIn profiles and content |
| **web_Scraper** | `81zGNiztzO6UFuUk` | General-purpose web scraper for extracting data |
| **Discord to Discord bot** | `IBPjSR6MfcVzGTzr` | Routes messages from one Discord server to bot-managed channels |

### 📚 Content & Publishing

| Workflow | ID | Purpose |
|----------|----|----|
| **Obsidian Notes Read Aloud: Available as a Podcast Feed** | `UgXQxMN2kkZ97Q7s` | Converts Obsidian notes into a podcast feed with audio |

### 🧪 Experimental & Development

| Workflow | ID | Purpose |
|----------|----|----|
| **My workflow 7** | `7CWHIbiWCQJtsTZt` | Development/test workflow |
| **My workflow 7.1** | `CcXM5F4azu7XvrL6` | Updated version of test workflow |
| **My workflow 8** | `y8gn08M1zeIQLMDZ` | Development/test workflow |

---

## 🚀 Quick Start

### Prerequisites
- n8n instance running (Docker or self-hosted)
- API credentials for integrations (GitHub, Gmail, Instagram, LinkedIn, etc.)
- Appropriate API keys for AI models (OpenAI, Google Gemini, Groq, etc.)

### Installation

1. **Export Workflows from n8n**
   ```bash
   # Workflows are auto-synced to this directory via GitHub backup automation
   # Manual export: In n8n UI → Workflow → Export
   ```

2. **Import a Workflow**
   - In n8n UI: **Workflows** → **Import from file**
   - Select the `.json` file from this directory
   - Configure credentials as needed
   - Activate and trigger

### Running Workflows

**Manual Trigger:**
- Open workflow in n8n UI
- Click **Execute Workflow** button

**Scheduled Execution:**
- Workflows with "Schedule Trigger" nodes run automatically at configured times
- View execution history in n8n dashboard

**Webhook Trigger:**
- Some workflows respond to external webhooks
- Check individual workflow configuration for webhook URLs

---

## 🔧 Configuration & Setup

### Common Setup Steps

1. **Add Credentials in n8n**
   ```
   Settings → Credentials → Create new
   ```
   
   Required for various workflows:
   - **GitHub**: Personal Access Token
   - **Gmail**: OAuth credentials
   - **Instagram**: API key
   - **LinkedIn**: API credentials
   - **OpenAI**: API key
   - **Google Gemini**: API key
   - **Groq**: API key

2. **Environment Variables** (in Docker)
   ```bash
   N8N_ENCRYPTION_KEY=your_key
   N8N_WEBHOOK_URL=http://localhost:5678
   ```

3. **Database Setup** (for persistence)
   ```bash
   # Docker compose includes PostgreSQL by default
   ```

---

## 📊 Workflow Categories & Use Cases

### Content Creation Pipeline
- **Input**: News sources, trending topics, user ideas
- **Process**: AI-powered generation, rephrasing, optimization
- **Output**: LinkedIn posts, Instagram captions, RSS feeds, podcasts

### Data Intelligence
- **Input**: Social media metrics, website traffic, news articles
- **Process**: Analysis, aggregation, AI insights
- **Output**: Reports, scheduling recommendations, optimized content calendars

### Integration & Sync
- **Input**: Multiple platforms (Instagram, LinkedIn, Discord, Gmail)
- **Process**: Data extraction, transformation, routing
- **Output**: Cross-platform publishing, organized feeds, automated responses

### Knowledge Management
- **Input**: Obsidian notes, archived content
- **Process**: Conversion, distribution
- **Output**: Podcast feeds, RSS feeds, readable formats

---

## 🔄 Workflow Status & Activity

| Type | Count |
|------|-------|
| **Active Workflows** | 28 |
| **Backup Workflows** | 2 |
| **News Workflows** | 7 |
| **AI/LLM Workflows** | 5 |
| **Scraper Workflows** | 4 |
| **Social Media Workflows** | 5 |

---

## 📝 Common Patterns

### Pattern 1: News Aggregation
```
Multiple news sources → Fetch articles → AI summarization → 
Discord/Telegram notification
```

### Pattern 2: Content Generation
```
User input/trending topic → AI generation → Format for platform → 
Schedule posting
```

### Pattern 3: Data Analysis
```
Platform API → Fetch metrics → AI analysis → Optimize schedule → 
Update recommendations
```

### Pattern 4: Cross-Platform Publishing
```
Content creation → Multi-platform formatting → Scheduled posting → 
Analytics tracking
```

---

## 🐛 Troubleshooting

### Workflow Not Executing
- ✅ Check if workflow is **Active** (toggle in UI)
- ✅ Verify **Schedule Trigger** time settings
- ✅ Check **Credentials** are valid and not expired
- ✅ Review **Execution logs** for error messages

### API Authentication Errors
- ✅ Verify API keys/tokens in credentials
- ✅ Check API rate limits
- ✅ Ensure API scopes match workflow requirements
- ✅ Rotate expired credentials

### Data Not Syncing
- ✅ Check webhook URLs are accessible
- ✅ Verify payload format matches expectations
- ✅ Check network connectivity
- ✅ Review error logs for details

### Memory/Performance Issues
- ✅ Use **Batch processing** for large datasets
- ✅ Limit **API response sizes** with filters
- ✅ Implement **rate limiting** between requests
- ✅ Archive old workflow executions

---

## 📚 Useful Resources

- [n8n Documentation](https://docs.n8n.io/)
- [n8n Community Forum](https://community.n8n.io/)
- [n8n Workflows Gallery](https://n8n.io/workflows/)
- [OpenAI API Docs](https://platform.openai.com/docs/)
- [Google Gemini API](https://ai.google.dev/)
- [GROQ API Docs](https://console.groq.com/docs/)

---

## 💡 Tips & Best Practices

✅ **Enable Logging**: Set `N8N_LOG_LEVEL=debug` for troubleshooting  
✅ **Use Staging**: Test on duplicate workflows before production use  
✅ **Monitor Executions**: Check dashboard regularly for failures  
✅ **Backup Regularly**: Use the backup workflows to sync to GitHub  
✅ **Update Credentials**: Rotate API keys periodically for security  
✅ **Document Changes**: Add notes when modifying workflows  

---

## 🤝 Contributing

To add or modify workflows:

1. Create/edit workflow in n8n UI
2. Test thoroughly in development
3. Export from n8n (Workflow → Export)
4. Commit `.json` file to repository
5. Update this README with workflow description

---

## 📄 License

These workflows are provided as-is for personal automation use.

---

## 📧 Support

For issues or questions:
- Check n8n logs in Docker: `docker logs n8n`
- Review workflow execution history in n8n UI
- Consult individual workflow documentation
- Check n8n community forums for similar issues

---

## Contact

- 📧 Email: [shahdeep1406@gmail.com](mailto:shahdeep1406@gmail.com)
- 🐙 GitHub: [DeepShah1406](https://github.com/DeepShah1406)
- 💼 LinkedIn: [deepshah1406](https://www.linkedin.com/in/deepshah1406)
- 🌐 Website: [Deep Shah](https://deepshah1406.github.io/)

---

**Last Updated**: December 2025  
**Total Workflows**: 28  
**Repository**: n8n-backup-demo
