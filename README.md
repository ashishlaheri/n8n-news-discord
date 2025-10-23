# n8n Automation: Tech News Summarizer & Discord Poster

This repository contains a workflow built in **n8n** that automates the process of fetching top tech news from an RSS feed, summarizing it using **Google Gemini (PaLM) AI**, performing a fun ping test, and posting everything to a **Discord** server. It's a simple example of combining **RSS feeds**, **AI summarization**, and **chat automation** in one workflow.

---

## Workflow Overview

1. **Manual Trigger**
   - The workflow starts when you click **Execute workflow** in n8n.

2. **RSS Feed Read**
   - Fetches the latest articles from [BleepingComputer RSS feed](https://www.bleepingcomputer.com/feed/).

3. **Limit Node**
   - Limits the number of RSS items processed to 5.

4. **AI Summarization**
   - Uses **Google Gemini Chat Model** via n8n LangChain nodes.
   - Summarizes each news article in **15 words**.

5. **Ping Test & Fun Output**
   - Executes a ping command (`ping 1.1.1.1 -c 4`).
   - Sends the output to Google Gemini for a **humorous summary** in 15 words, inspired by Ryan Reynolds style.

6. **Merge Node**
   - Combines the summarized news and the ping output.

7. **Discord Integration**
   - Posts the final content to a Discord channel via **webhook**.
   - Includes article title, creator, link, publication date, summary, and fun ping message.

---

## Tech Stack

- **n8n** – Workflow automation
- **RSS Feeds** – Fetch latest tech news
- **Google Gemini (PaLM API)** – AI summarization & fun message generation
- **Discord Webhook** – Message delivery
- **LangChain Nodes** – AI integration in n8n

---

## How to Use

1. Clone this repository.
2. Import the workflow JSON file into **n8n**.
3. Set up the following credentials in n8n:
   - **Google Gemini (PaLM) API**
   - **Discord Webhook**
4. Click **Execute workflow** to fetch news, summarize, and post to Discord.

---

## Outcome

- Summarized top 5 tech news articles daily.
- Fun ping output for system testing.
- Automatic posting to Discord for easy access.
- Demonstrates **n8n + AI + automation** integration in a single workflow.

---

## Future Improvements

- Add multiple RSS feeds.
- Include scheduling to automate daily posts.
- Enhance AI output formatting with markdown or embeds for Discord.
