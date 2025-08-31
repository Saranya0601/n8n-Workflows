# n8n-Workflows
n8n Workflows  ----  Gmail Automation , Telegram bot, LinkedIn Content Automation, Notion + LinkedIn Automation (Scheduled) .

**1. Gmail Automation**

_How it works:_

A chat message comes in → triggers the flow.

The message is passed to the AI Agent.

The OpenAI Chat Model interprets the message and creates a response.

Window Buffer Memory keeps track of conversation history (so the AI remembers context).

The response is sent to Gmail, which delivers it as an email.

👉 This means your chatbot can automatically respond to users and send them emails with the answers.

**🔹 2. Telegram Bot**

_How it works:_

A user sends a message on Telegram → workflow triggers.

Message goes to the AI Agent.

The agent decides whether to:

Generate a conversational response (via OpenAI Chat Model).

Fetch factual info (via Wikipedia).

Search the web (via SerpAPI).

The AI Agent merges results from these tools.

Sends the final response back to the Telegram user.

👉 This creates an AI-powered Telegram bot that can answer conversational, factual, and search-based questions.

**🔹 3. LinkedIn Content Automation**

_How it works:_

A chat message (or API feed) comes in.

An HTTP Request retrieves external content (e.g., RSS news, blog posts).

XML → JSON converts the data into structured format.

Split Out / Edit Fields / Aggregate → cleans & processes the content.

Loop Over Items → cycles through multiple posts.

AI (LinkedIn Post Generator) → creates a LinkedIn-friendly post.

Wait node → controls posting schedule (so posts don’t go all at once).

Posts are saved into Google Sheets for record-keeping.

👉 This workflow automates social media content creation — pulling info from external sources and transforming it into ready-to-post LinkedIn updates.

**🔹 4. Notion + LinkedIn Automation (Scheduled)**

_How it works:_

A Schedule Trigger runs the flow at fixed times (e.g., daily).

Notion nodes fetch data/content ideas from your Notion database.

Aggregate merges the fetched content into a structured format.

Google Gemini Chat Model generates professional LinkedIn posts from the Notion data.

AI Agent adds reasoning and tool usage if needed.

HTTP Request can pull additional context (e.g., trending news or stats).

Merge combines Gemini’s text + external data.

LinkedIn node publishes the final post directly.

👉 This is a fully automated LinkedIn posting system where you just update Notion, and the workflow does the rest (content creation + posting).
