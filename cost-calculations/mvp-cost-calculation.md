# MVP Cost Calculation for Hackathon
## Personal AI Health Assistant - Budget Breakdown

---

## 💰 Total MVP Cost: **$135 - $285** (₹11,250 - ₹23,750)

### Cost Breakdown for 1-Month Hackathon Period

---

## 1. AI API Costs (Testing & Demo)

### OpenAI API (GPT-4 & Embeddings)
**Assumptions for Testing:**
- 500 test conversations
- Average 10 messages per conversation = 5,000 messages
- Average tokens per message: 500 input + 300 output = 800 tokens
- Total tokens: 5,000 × 800 = 4,000,000 tokens

**GPT-4 Turbo Pricing:**
- Input: $10 per 1M tokens
- Output: $30 per 1M tokens
- Input cost: (2,500,000 tokens / 1M) × $10 = **$25**
- Output cost: (1,500,000 tokens / 1M) × $30 = **$45**
- **GPT-4 Total: $70**

**Embeddings (text-embedding-3-small):**
- 10,000 documents/chunks to embed
- Average 500 tokens per chunk = 5,000,000 tokens
- Pricing: $0.02 per 1M tokens
- Cost: (5M / 1M) × $0.02 = **$0.10**

**OpenAI Total: $70.10**

### Alternative: Use GPT-3.5-Turbo (Budget Option)
- Input: $0.50 per 1M tokens
- Output: $1.50 per 1M tokens
- Input cost: (2.5M / 1M) × $0.50 = **$1.25**
- Output cost: (1.5M / 1M) × $1.50 = **$2.25**
- **GPT-3.5 Total: $3.50** (saves $66.50)

### Google Gemini API (For OCR & Multimodal)
**Assumptions:**
- 200 document images to process
- Gemini 1.5 Flash (free tier: 15 requests/min, 1M tokens/day)
- **Cost: $0** (within free tier limits)

### Anthropic Claude (Optional - for document analysis)
**If needed:**
- Claude 3.5 Haiku: $0.25 per 1M input tokens
- 100 document analysis requests × 10,000 tokens = 1M tokens
- **Cost: $0.25** (optional)

**AI API Total (Conservative): $70 - $75**
**AI API Total (Budget with GPT-3.5): $4 - $5**

---

## 2. Cloud Infrastructure (Testing & Deployment)

### Option A: AWS Free Tier (Recommended for Hackathon)
**Free for 12 months:**
- EC2 t2.micro: 750 hours/month (FREE)
- RDS PostgreSQL t3.micro: 750 hours/month (FREE)
- S3: 5GB storage (FREE)
- Lambda: 1M requests/month (FREE)
- **Cost: $0**

**Additional Services (Paid):**
- Elastic IP (if needed): $3.60/month
- Data transfer out: ~$1-2/month for testing
- **AWS Total: $5 - $10/month**

### Option B: Google Cloud Platform (GCP)
**Free Tier:**
- Compute Engine e2-micro: 1 instance (FREE)
- Cloud SQL: Not in free tier
- Cloud Storage: 5GB (FREE)

**Paid Services:**
- Cloud SQL (db-f1-micro): $7/month
- **GCP Total: $7 - $12/month**

### Option C: Railway.app / Render.com (Easiest for Hackathon)
**Railway.app:**
- $5 free credit for new users
- Hobby plan: $5/month (includes PostgreSQL, Redis)
- **Cost: $0 - $5** (with free credit)

**Render.com:**
- Free tier: Web service + PostgreSQL
- Limitations: Spins down after inactivity
- **Cost: $0** (free tier sufficient for demo)

**Cloud Infrastructure Total: $0 - $10/month**

---

## 3. Vector Database

### Pinecone
**Free Tier (Starter):**
- 1 pod (sufficient for testing)
- 100K vectors
- **Cost: $0** (free tier)

### Alternative: ChromaDB (Self-hosted)
- Open-source, runs on your cloud instance
- **Cost: $0** (included in cloud compute)

**Vector DB Total: $0**

---

## 4. Domain & Hosting

### Domain Registration
**Options:**
- .com domain: $10 - $15/year
- .in domain: $8 - $12/year
- .ai domain: $60 - $80/year (premium)

**Recommended:** .in or .com domain
**Cost: $10 - $15** (one-time for year)

### SSL Certificate
- Let's Encrypt: **FREE**
- Cloudflare SSL: **FREE**

**Domain Total: $10 - $15**

---

## 5. Mobile App Deployment

### Google Play Store
- One-time developer registration: **$25**
- App publishing: FREE
- **Cost: $25** (one-time)

### Apple App Store (Optional)
- Annual developer fee: $99/year
- **Cost: $99** (skip for hackathon if budget-constrained)

**Mobile Deployment Total: $25** (Android only)

---

## 6. Additional Services

### Redis Cache
**Options:**
- Redis Cloud Free Tier: 30MB (sufficient for testing)
- **Cost: $0**

### Monitoring & Logging
**Free Tiers:**
- Sentry: 5K errors/month (FREE)
- LogRocket: 1K sessions/month (FREE)
- **Cost: $0**

### Email Service (for notifications)
**SendGrid:**
- Free tier: 100 emails/day
- **Cost: $0**

### SMS Service (for OTP/reminders)
**Twilio:**
- Trial credit: $15 (FREE)
- After trial: $0.0079 per SMS (India)
- 100 test SMS = $0.79
- **Cost: $0 - $1**

**Additional Services Total: $0 - $1**

---

## 📊 Final Cost Breakdown

### Conservative Estimate (Using GPT-4)
| Item | Cost |
|------|------|
| AI API (OpenAI GPT-4 + Embeddings) | $70 |
| Cloud Infrastructure (AWS Free Tier) | $10 |
| Vector Database (Pinecone Free) | $0 |
| Domain Registration (.in) | $10 |
| Google Play Store | $25 |
| Additional Services | $1 |
| **TOTAL** | **$116** |

### Budget Estimate (Using GPT-3.5)
| Item | Cost |
|------|------|
| AI API (OpenAI GPT-3.5 + Embeddings) | $5 |
| Cloud Infrastructure (Render.com Free) | $0 |
| Vector Database (ChromaDB Self-hosted) | $0 |
| Domain Registration (.in) | $10 |
| Google Play Store | $25 |
| Additional Services | $0 |
| **TOTAL** | **$40** |

### Recommended Hackathon Budget
| Item | Cost |
|------|------|
| AI API (Mix: GPT-4 for demo, GPT-3.5 for testing) | $30 |
| Cloud Infrastructure (Railway.app with free credit) | $5 |
| Vector Database (Pinecone Free Tier) | $0 |
| Domain Registration (.com) | $12 |
| Google Play Store | $25 |
| Additional Services (SMS testing) | $1 |
| **TOTAL** | **$73** |

---

## 💡 Cost Optimization Tips for Hackathon

### 1. Use Free Tiers Aggressively
- AWS/GCP free tier for compute
- Pinecone free tier for vector DB
- Render.com/Railway.app for easy deployment
- Gemini API free tier for OCR

### 2. Optimize AI API Usage
- Use GPT-3.5-Turbo for testing ($0.50/1M tokens)
- Use GPT-4 only for final demo and critical features
- Cache common responses in Redis
- Implement rate limiting to prevent accidental overuse

### 3. Use Open Source Alternatives
- ChromaDB instead of Pinecone (self-hosted)
- Ollama for local LLM testing (free)
- Tesseract OCR instead of cloud OCR APIs

### 4. Delay Non-Essential Costs
- Skip iOS deployment ($99) - focus on Android
- Use free domain from education programs (if available)
- Use subdomain from free hosting (e.g., yourapp.railway.app)

### 5. Student/Startup Credits
- **GitHub Student Pack**: $200 Azure credit, $100 DigitalOcean
- **AWS Educate**: $100 credit for students
- **Google Cloud**: $300 free credit for new users
- **OpenAI**: Apply for startup credits (if eligible)

---

## 🎯 Recommended Hackathon Budget

### Minimal Viable Budget: **$40 - $50**
- Use all free tiers
- GPT-3.5 for most operations
- Free hosting (Render.com)
- Skip domain (use free subdomain)
- Android only

### Comfortable Budget: **$70 - $100**
- Mix of GPT-3.5 and GPT-4
- Railway.app hosting ($5)
- Custom domain ($12)
- Android deployment ($25)
- SMS testing ($1)

### Professional Demo Budget: **$150 - $200**
- GPT-4 for all demo interactions
- Stable cloud hosting (AWS/GCP)
- Custom domain with SSL
- Both Android and iOS
- Professional monitoring tools

---

## 📝 Cost Tracking Recommendations

### Set Up Billing Alerts
1. **OpenAI**: Set usage limits in dashboard ($50 max)
2. **AWS**: Create billing alarm at $10, $25, $50
3. **GCP**: Set budget alerts
4. **Monitor daily**: Check API usage dashboards

### Use Cost Calculators
- OpenAI Token Counter: https://platform.openai.com/tokenizer
- AWS Pricing Calculator: https://calculator.aws/
- GCP Pricing Calculator: https://cloud.google.com/products/calculator

---

## 🚀 Zero-Cost Hackathon Option (If Needed)

If budget is extremely tight, here's a **$25 option** (Play Store only):

| Item | Cost | How |
|------|------|-----|
| AI API | $0 | Use Gemini API free tier (1M tokens/day) |
| Cloud | $0 | Render.com free tier |
| Vector DB | $0 | ChromaDB self-hosted |
| Domain | $0 | Use free subdomain (yourapp.render.com) |
| Play Store | $25 | Required for Android |
| **TOTAL** | **$25** | |

**Limitations:**
- Slower response times (free tier limits)
- App spins down after inactivity
- No custom domain
- Limited to Gemini API capabilities

---

## 💰 Currency Conversion (Approximate)

**$73 (Recommended)** = ₹6,000 - ₹6,100  
**$40 (Budget)** = ₹3,300 - ₹3,400  
**$150 (Professional)** = ₹12,500 - ₹12,600  

*Exchange rate: $1 = ₹83 (Feb 2026)*

---

## ✅ Final Recommendation for Hackathon

**Budget: $70 - $100** (₹5,800 - ₹8,300)

This provides:
- ✅ Professional demo with GPT-4
- ✅ Reliable hosting
- ✅ Custom domain
- ✅ Android app on Play Store
- ✅ Room for testing and iterations
- ✅ Professional presentation

**Start with free tiers, scale up only if needed during hackathon!**

---

*Cost Calculation Version 1.0 | February 2026*
*Based on current API pricing and free tier offerings*
