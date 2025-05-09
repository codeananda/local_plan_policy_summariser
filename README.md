# 🚀Automated UK Local Plan Policy Summariser

![generated-image (1) copy](https://github.com/user-attachments/assets/1e99d5da-537f-4769-8d49-5fc971f9c6a2)


## 🎯 Problem Statement

Each UK district publishes a 300–1,000-page Local Plan PDF containing 50–100 individual policies. Manual review is time-consuming, error-prone and fails to scale as plans update, leaving developers and planners without instant, reliable policy insights.

## ⚙️ Technical Approach

* Use Google Gemini’s 2M-token, multimodal context to ingest full documents and retain full document understanding  
* Orchestrate LLM calls with LangChain for provider-agnostic switching  
* Build custom chunking to respect LLM size limits  
* Leverage Anthropic’s Claude for targeted policy extraction and precise formatting  
* Containerise with Docker & Poetry; deploy on AWS (EC2, ECR, RDS, S3)  
* Manage idempotent upserts in Postgres; track processed docs  
* Implement caching at the LLM layer to slash compute costs by 75%

## 🛠 Skills

Python · OpenAI API · LangChain · Poetry · Docker · PostgreSQL (AWS RDS) · AWS S3 · AWS EC2 · Google Gemini 1.5 Pro · Google Vertex AI · Anthropic Claude · custom PDF chunking · LLM caching strategies · multi-LLM pipeline · modular Python architecture · Slack webhook logging

## 🔧 Challenges & Solutions

* PDF formatting loss with python libraries → resolved with Gemini’s native multimodality  
* Max file size constraints → custom chunking strategy to ensure all documents are below the threshold  
* Escalating LLM costs → caching layer & switch to Vertex AI for large docs (AI Studio had a bug which meant it would not cache large documents)  
* Inconsistent extractions → hybrid Gemini \+ Claude workflow  
* Deployment complexity → modularised codebase, clear naming, extensive logging & Slack alerts

## 📊 Quantifiable Business Impact

* 75% reduction in LLM spend  
* Fully automated weekly pipeline handling 700+ plans  
* Instant policy summaries and Q\&A via LandGPT (the client’s chatbot)  
* Scalable, maintainable architecture with plug-and-play policy modules

## ⭐ Client Review

<img width="933" alt="Screenshot 2025-05-09 at 13 14 02" src="https://github.com/user-attachments/assets/9b0c4c3a-8882-42e9-be76-6e4b9f340ffe" />


*Note: this was one project of many from a long-term contract with the above client*
