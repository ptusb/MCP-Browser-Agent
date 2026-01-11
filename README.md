# 🌐 MCP-Browser-Agent

**Autonomous Web Navigation & Scraping Engine | Architected by [Piyush Deepak Tayade](https://github.com/ptusb)**

[![Status: Production-Ready](https://img.shields.io/badge/Status-Production--Ready-blue)](https://github.com/ptusb)
[![Playwright](https://img.shields.io/badge/Interface-Playwright-green)](https://playwright.dev)
[![MCP-Powered](https://img.shields.io/badge/Bridge-MCP-green)](https://modelcontextprotocol.io)

A professional Model Context Protocol (MCP) server that grants LLMs (Claude/GPT) the ability to browse the live web, interact with complex SPAs, and extract structured data using **Playwright**. This is the entry point for building "Autonomous Research Agents."

---

## 💼 Strategic Deep Dive (For Leadership)

### **Why this project exists? (The Problem)**

Traditional LLMs are cut off from the live web or rely on basic scrapers that fail on JavaScript-heavy sites. This project allows AI to "see" and "interact" with the web just like a human does, overcoming the limitations of static training data.

### **How it works? (The Solution)**

This is a **System-Level Browser Controller**.

1. **Headless Execution:** It spawns a headless Chromium instance via Playwright.
2. **MCP Tools:** It exposes tools like `navigate_to`, `click_element`, `extract_text`, and `take_screenshot` to the AI.
3. **Real-time Interaction:** The AI can "think" about a multi-step web task (e.g., "Find the price and stock of X on site Y and site Z") and execute it sequentially.

### **What is the result? (The Impact)**

- **Market Intel at Scale:** Automate competitive research that used to take human analysts hours.
- **Dynamic Site Interaction:** Reach beyond simple URLs to handle logins, forms, and dynamic data loads.

---

## 🙋 Potential Interview/Boss Questions (Ready-to-Answer)

**Q: "How do you handle bot detection on modern sites?"**
- **A:** *"We use 'Playwright-Stealth' configurations and human-like interaction curves (non-linear mouse movement and randomized delays). It’s designed to be a 'Concierge' agent, not a brute-force scraper."*

**Q: "Is it expensive to run a browser for every AI query?"**
- **A:** *"We use 'Headless Mode' and 'Resource Blocking' (disabling images/stylesheets when not needed) to minimize CPU and RAM overhead, ensuring it stays cost-effective for enterprise use."*

---

## ⚙️ Implementation Guide (Step-by-Step)

### **1. Prerequisites**

- Install **Node.js** (v18+)
- Install **Playwright Browsers**: `npx playwright install chromium`

### **2. Installation**

```bash
git clone https://github.com/ptusb/MCP-Browser-Agent.git
cd MCP-Browser-Agent
npm install
npm run build
```

### **3. Configuration**

Add to `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "browser-agent": {
      "command": "node",
      "args": ["C:\\path\\to\\MCP-Browser-Agent\\dist\\index.js"]
    }
  }
}
```

---

## 🎬 Demonstration Guide (How to see it in Action)

1. **Launch Claude**: Enable the `browser-agent` tool.
2. **Input Prompt**:
    > *"Navigate to news.ycombinator.com, find the top 5 trending AI stories, and give me a summary of each."*
3. **Observation**: You will see Claude opening the browser, scraping the titles, and then navigating into each story to read the content.
4. **Verification**: You will receive a high-velocity research report based on data that is only minutes old.

---

## 🚀 Key Features

- **Full DOM Control:** Interaction with any CSS selector.
- **Visual Verification:** Automated screenshots or PDFs of web pages.
- **Secure Sandbox:** Operations occur in an isolated browser context.
