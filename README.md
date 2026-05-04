# Scholar Stream Pro 🎓
**AI-Driven Academic Research & Intelligent Citation Engine**

[🚀 View Live Demo on Hugging Face Spaces] (https://huggingface.co/spaces/mubashrawaqar123/scholar-stream-pro)

## 🌟 Overview
Scholar Stream Pro is a specialized tool designed to solve the "information overload" problem in academia. Built during an intensive development sprint, this application automates the process of finding relevant research papers, synthesizing their findings using high-speed LLMs, and formatting citations instantly.

## 🧠 Why I Built This
Researchers often spend hours filtering through search results. I wanted to create a "streamlined" experience where the AI does the initial reading for you, providing a summarized "stream" of knowledge so you can decide which papers deserve a deep dive.

## 🚀 Key Features
*   **Instant Summarization:** Powered by Groq's LPU inference engine for lightning-fast abstract analysis.
*   **Hybrid Search Logic:** Unlike standard tools that rely on a single database, this app cross-references multiple sources.
*   **One-Click Citations:** Automatically generates citations to save time during the drafting phase.

## 🛠️ The "Hybrid" Search Advantage
For this project, I moved away from relying solely on the **Semantic Scholar API**. Instead, the backend utilizes a combination of official APIs and targeted web-based data retrieval.
*   **Reliability:** Relying on a single API can lead to "single point of failure." If one service is down or rate-limited, the hybrid system pulls from alternative web sources.
*   **Data Freshness:** Academic APIs sometimes have a lag in indexing. By incorporating web-based fetching, the tool can surface more recent publications and "gray literature" that hasn't been fully indexed yet.

## 💻 Technical Stack
*   **Interface:** Gradio (optimized for rapid deployment)
*   **LLM Logic:** Groq Cloud API
*   **Search Engine:** Semantic Scholar API + Web Scraper modules
*   **Language:** Python

### 🔑 Required API Keys
To run this project, you will need to configure two environment variables:
* **scholarApi**: Used for the Groq Cloud LLM (this handles the AI summarization).
* **scholar_api_key**: Used for the Semantic Scholar API (this handles fetching the research papers).
## 📥 How to Use (For Recruiters/Developers)
1. **Clone:** `git clone https://github.com/yourusername/scholar-stream-pro.git`
2. **Environment:** Set your API keys as environment variables (`scholarApi` and `scholar_api_key`).
3. **Run:** Execute `python app.py` to launch the Gradio interface.
