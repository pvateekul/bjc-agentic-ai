# OpenClaw Demo Prompts

This document contains all prompts used in the OpenClaw presentation and demonstrations.

> **Note:** Replace all placeholders in the format `<...>` with values appropriate for your use case before running the prompts.

---

## 0. Hatch the Agent — Identity Setup Prompt **<font color='red'>(Skip)</font>**

$${\\color{red}You \\space can \\space skip \\space this \\space lab!}$$

> Use this prompt in `#main` channel.  

Use this prompt to initialize the agent's identity, personality, timezone, and behavioral boundaries.

```md
Hi, I'm <your-name>. You are OpenClaw, my AI assistant. You can call me <your-name>. I want you to have a calm vibe.

Please set our timezone to Thailand/Bangkok. You can pick up any emoji of your choice.
For my boundaries:
- Private things stay private.
- When in doubt, ask before acting externally.
- Never sand half-baked replies to messaging surfaces.
- You are not user's voice - be carreful in group chats.
```

---

## 1. Basic Interaction with OpenClaw

> Use these prompts in the `#main` channel.  
> This lab should take around 2 minutes.  

Use the following prompts to explore OpenClaw's basic conversational capabilities.

### 1.1 Ask about OpenClaw

```md
@<OpenClaw> What is your name?
@<OpenClaw> What can you do?
@<OpenClaw> What is your role in this Discord server?
```

### 1.2 Ask General Questions

```md
@<OpenClaw> Explain what artificial intelligence is in one paragraph.
@<OpenClaw> What are three interesting facts about Thailand?
```

### 1.3 Test Reasoning and Mathematics

```md
@<OpenClaw> What is 125 × 48?
@<OpenClaw> If a train travels 120 km in 2 hours, what is its average speed?
```

### 1.4 Test Creative Responses

```md
@<OpenClaw> Write a short motivational quote for students.
@<OpenClaw> Suggest three ideas for a weekend project.
```

Feel free to ask your own questions and continue the conversation to explore OpenClaw's capabilities.

---

## 2. Markdown Generation Prompt

> Use this prompt in the `#main` channel.  
> This lab should take around 2 minutes.  

Use this prompt to generate a markdown file showcasing OpenClaw capabilities.

```md
@<OpenClaw> Generate a concise and professional `README.md` based on the provided project documentation and source code.

Include:
* Project title and brief description
* Key features and capabilities
* High-level architecture/workflow summary
* Installation instructions
* Quick start guide
* Basic usage examples
* Project structure overview
* Contribution and license sections

Requirements:
* Use clean GitHub-flavored Markdown
* Keep the README concise and easy to read
* Include code blocks where helpful
* Use headings, bullet points, and badges where appropriate
* Return only Markdown content
```

After generating the Markdown file, use the following prompt to post it back to the current Discord channel:

```md
@<OpenClaw> Please send the generated Markdown file back to this Discord channel.
```

---

## 3. Food Price Analysis Automation

> Use this prompt in the `#main` channel.  
> This lab should take around 3 minutes.  

Use this prompt to analyze food price volatility and identify the most unstable food items in the dataset.

```md
@<OpenClaw> Please analyze the dataset `food_prices.csv`. Identify the top 5 food items with the highest price volatility and provide appropriate visualizations to support your findings.
```

> Don't forget to insert `food_prices.csv` in Discord channel.   
[Link to file](./assets/food_prices.csv)

---

## 4. Testing News Searching Agent

> Use this prompt in the `#news` channel.  
> This lab should take around 1 minutes.  

Use this prompt to test the news search and retrieval capability.

```md
@<OpenClaw> ช่วยหาข่าวเกี่ยวกับ <หัวข้อ>
```

**Example:**

```md
@<OpenClaw> ช่วยหาข่าวเกี่ยวกับ AI
```

---

## 5. Testing News Content Agent

> Use this prompt in the `#content` channel.  
> This lab should take around 1 minutes.  
> This lab is a continuation of the previous lab (Testing News Searching Agent).  

You can copy selected news content and source references from the **News Searching Agent** output and paste them directly into the content channel.

```md
@<OpenClaw> ช่วยเขียนข่าวเกี่ยวกับ <เนื้อหาข่าว>
```

**Example:**

```md
@<OpenClaw> ช่วยเขียนข่าวเกี่ยวกับ AP รายงานว่าหลายรัฐในสหรัฐยังเดินหน้ากำกับ AI ต่อ แม้ฝั่งทรัมป์จะเคยกดดันไม่ให้รัฐออกกฎเอง https://apnews.com/article/trump-artificial-intelligence-chatbots-ai-23a0e44ab05402ddfe9cdfd0bffa0ade
```

---

## 6. AI Agent Custom Skill with OpenClaw

> Use this prompt in the `#main` channel.  
> This lab should take around 3 minutes.  

Use this prompt to demonstrate custom skill execution using the `vo-to-slides` skill.

```md
@<OpenClaw> Can you help make a simple slide based on the topic; <TOPIC>. 
Please use this skill https://github.com/Samin12/vo-to-slides, download this skill and make some slides so that I can look through it and present it.
```

**Example:**

```md
@<OpenClaw> Can you help make a simple slide based on the topic; `AI for food industry`. 
Please use this skill https://github.com/Samin12/vo-to-slides, download this skill and make some slides so that I can look through it and present it.
```

After generating the `.pptx` file, use the following prompt to post it back to the current Discord channel:

```md
@<OpenClaw> Please send the generated `.pptx` file back to this Discord channel.
```

---

**End of Document**