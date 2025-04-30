# 🎮 Forge Your Team – VCT Hackathon Submission

A smart scouting assistant for Valorant esports teams, built for the AWS x Riot Games VCT Hackathon. It uses real-world player stats and an LLM-powered backend to generate team compositions, justify picks, and answer detailed questions about player performance and strategy.

---

## 🎯 Purpose

Forge Your Team addresses key scouting challenges in esports:

- 🔍 Find top players by region, role, or performance
- 🧠 Build optimized teams based on criteria like skill level, region, or gender
- 🗣️ Answer questions like "Who is a good IGL from NA?" or "Build a strong controller-heavy team for EMEA"

---

## 🚀 Features

- 🧑‍💻 **Team Composition Builder** – Generates 5-player teams with assigned roles based on prompts
- 📊 **Player Stats & Role Insights** – Pulls in agent preferences, top stats, and region info
- 📦 **Retrieval-Augmented Generation (RAG)** – Combines structured data with LLM responses for factual accuracy
- 🌐 **LLM-Powered Chat Interface** – Ask questions like:
  - “Give me a team with a strong IGL and duelist duo from NA”
  - “Who’s a rising talent controller from the APAC region?”

---

## 🧰 Tech Stack

| Layer          | Tools/Services                         |
|----------------|----------------------------------------|
| Frontend       | Streamlit                              |
| LLM Backend    | Amazon Bedrock (Claude/GPT via RAG)    |
| Data Layer     | Pandas, AWS S3                         |
| Serverless     | AWS Lambda                             |
| Integration    | LangChain (optional), boto3            |

---

## 📁 Repo Structure

```
vct_hackathon_frkd/
├── data/                      # Preprocessed and raw player data
├── prompts/                   # Prompt templates for RAG / LLM
├── main_app.py                # Streamlit interface
├── lambda_handler.py          # AWS Lambda integration
├── rag_utils.py               # RAG + context management logic
├── generate_team.py           # LLM-based team building logic
├── analyze_player.py          # Player-level analysis
├── requirements.txt
└── README.md
```

---

## 🧪 Setup Instructions

1. Clone the repo:
   ```bash
   git clone https://github.com/veeoid/vct_hackathon_frkd.git
   cd vct_hackathon_frkd
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run locally:
   ```bash
   streamlit run main_app.py
   ```

4. To deploy backend as Lambda:
   - Zip `lambda_handler.py` and dependencies
   - Upload to AWS Lambda
   - Set environment variables for API keys

---

## 🧠 Sample Prompt Ideas

- “Build a mixed-gender Valorant team with players from EMEA”
- “Who is the best duelist from Brazil in the past 6 months?”
- “Recommend a support player with consistent K/D across events”

---

## 🧵 Learnings

- Integrated structured esports data into real-time LLM chat experience
- Designed and deployed serverless functions with Bedrock LLMs
- Gained deep insight into RAG design and streamlit-based rapid prototyping

---

## 👤 Author

**Vismay Chaudhari**  
🔗 [Portfolio](https://portfolio-ca88.vercel.app) · [LinkedIn](https://linkedin.com/in/vismay-chaudhari)

---

## 📄 License

MIT License (or add your own)

---

_This project was built as part of the AWS x Riot Games VCT Hackathon challenge._
