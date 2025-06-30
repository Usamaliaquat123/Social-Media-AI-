# Instig8.AI Viral OS

A powerful N8N workflow automation system for social media content analysis and viral content strategy generation.

## 🚀 Overview

Instig8.AI Viral OS is an automated workflow that helps content creators and marketers:
- Scrape and analyze content from 6 major social platforms
- Perform sentiment analysis on audience engagement
- Generate AI-powered viral content playbooks
- Track top-performing content across platforms

## 📋 Features

### Supported Platforms
- ✅ TikTok
- ✅ Instagram  
- ✅ YouTube
- ✅ Twitter/X
- ✅ LinkedIn
- ✅ Facebook

### Core Capabilities

1. **🔨 Content Scraping**
   - Scrape posts based on hashtags or profiles
   - Filter high-performing content
   - Extract engagement metrics (likes, shares, comments, views)
   - Download transcripts and captions

2. **📄 Engagement Analysis**
   - Sentiment analysis on comments (1-5 scale)
   - Tool usefulness scoring
   - Extract common questions from audience
   - Generate key insights from engagement patterns

3. **🏆 Viral Playbook Generation**
   - AI-generated content strategies
   - Hook creation and script writing
   - Audience avatar development
   - SEO optimization recommendations
   - Cross-platform repurposing angles

## 🛠️ Prerequisites

### Required Services
- N8N instance (self-hosted or cloud)
- Airtable account with configured base
- Google Drive account (for playbook storage)
- OpenAI API key (GPT-4 access)
- Apify API key (for social media scraping)

### API Credentials Needed
- Airtable Personal Access Token
- Google Drive OAuth2
- OpenAI API
- Apify API Token

## 📦 Installation

1. **Import the Workflow**
   ```bash
   # In your N8N instance, go to Workflows > Import
   # Upload the product.json file
   ```

2. **Configure Credentials**
   - Navigate to Credentials in N8N
   - Add the required API credentials listed above
   - Map credentials to the appropriate nodes

3. **Set Up Airtable Base**
   - Create tables matching the workflow structure:
     - 🤖 Automations
     - 📃 Inputs  
     - 📚 Audience Intelligence

4. **Configure Webhook**
   - Note the webhook URL from the Webhook node
   - Use this to trigger automations

## 🎯 Usage

### Triggering Automations

Send a webhook request with the following structure:
```json
{
  "query": {
    "recordId": "YOUR_AIRTABLE_RECORD_ID"
  }
}
```

### Automation Types

1. **Run Scraper**
   - Set up input profiles/hashtags in Airtable
   - Configure quantity to scrape
   - Select social channels

2. **Analyze Engagement Signals**
   - Automatically triggered after scraping
   - Processes comments for sentiment analysis
   - Updates Airtable with insights

3. **Generate Viral Playbook**
   - Analyzes top-performing content
   - Creates comprehensive content strategy
   - Outputs to Google Docs

## 📊 Data Flow

```
Webhook Trigger → Airtable Config → Social Platform Scrapers
                                           ↓
                                    Comment Analysis
                                           ↓
                                    Sentiment Scoring
                                           ↓
                                    Airtable Storage
                                           ↓
                                    Viral Playbook Generation
                                           ↓
                                    Google Docs Export
```

## ⚙️ Configuration

### Airtable Schema

**🤖 Automations Table**
- Type of Automation (Single Select)
- Social Channel (Multi-select)
- Quantity to Scrape (Number)
- Status (Single Select)
- Run Automation (Checkbox)

**📃 Inputs Table**
- Channel (Single Select)
- Type (Profile/Hashtag)
- Hashtag/Username (Text)
- Active (Single Select)

**📚 Audience Intelligence Table**
- All scraped content metrics
- Sentiment analysis results
- Viral playbook links

### Customization Options

- Adjust scraping limits in HTTP Request nodes
- Modify sentiment analysis prompts in OpenAI nodes
- Customize viral playbook template in the AI generation node
- Configure minimum engagement thresholds

## 🔍 Monitoring

- Check Airtable for automation status updates
- Review execution logs in N8N
- Monitor API usage for rate limits

## ⚠️ Important Notes

- Respect platform rate limits and terms of service
- API costs can accumulate with high-volume usage
- Ensure proper data privacy compliance
- Test with small batches before scaling

## 🤝 Contributing

To contribute improvements:
1. Export your modified workflow
2. Document changes clearly
3. Test thoroughly
4. Share via pull request or issue

## 📄 License

This workflow is provided as-is for educational and commercial use. Please ensure compliance with all third-party service terms.

## 🆘 Support

For issues or questions:
- Check N8N documentation
- Review API service documentation
- Verify Airtable field mappings
- Ensure all credentials are properly configured

---

Built with ❤️ using N8N workflow automation
