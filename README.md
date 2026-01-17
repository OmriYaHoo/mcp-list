# MCP Servers List

A comprehensive list of MCP (Model Context Protocol) servers compiled from various YouTube videos.

---

## Table of Contents

- **[Development & Debugging](#development--debugging)** (7): [Sentry](#sentry-mcp-server), [SpotlightJS](#spotlightjs-mcp-server), [Chrome DevTools](#chrome-devtools-mcp-server), [Playwright](#playwright-mcp-server), [Browser MCP](#browser-mcp), [Sequential Thinking](#sequential-thinking-mcp-server), [Vibe Check](#vibe-check-mcp)
- **[Documentation & Research](#documentation--research)** (3): [Context7](#context7-mcp-server), [Ref](#ref-mcp-server), [Perplexity](#perplexity-mcp)
- **[Framework-Specific](#framework-specific)** (4): [Nuxt](#nuxt-mcp-server), [Svelte](#svelte-mcp-server), [Flutter](#flutter-mcp), [Shadcn Registry](#shadcn-registry-mcp-server)
- **[Cloud & Infrastructure](#cloud--infrastructure)** (4): [Cloudflare](#cloudflare-mcp-servers), [Vercel](#vercel-mcp-server), [Docker](#docker-mcp), [Kubernetes](#kubernetes-mcp)
- **[Google Services](#google-services)** (5): [Google Maps](#google-maps-mcp), [BigQuery](#bigquery-mcp), [Google Compute](#google-compute-mcp), [Google Workspace](#google-workspace-mcp), [Google Analytics](#google-analytics-mcp)
- **[Database & Backend](#database--backend)** (2): [Supabase](#supabase-mcp-server), [Firebase](#firebase-mcp)
- **[Payments & Business](#payments--business)** (1): [Stripe](#stripe-mcp-server)
- **[Project Management & Productivity](#project-management--productivity)** (4): [Linear](#linear-mcp), [GitHub](#github-mcp), [Notion](#notion-mcp), [Obsidian](#obsidian-mcp)
- **[Data & Web Scraping](#data--web-scraping)** (1): [Apify](#apify-mcp-server)
- **[Security](#security)** (1): [Semgrep](#semgrep-mcp)
- **[Voice & Communication](#voice--communication)** (1): [11 Labs](#11-labs-mcp-server)
- **[Memory & Context](#memory--context)** (1): [Pieces](#pieces-mcp)
- **[Workflow & Orchestration](#workflow--orchestration)** (1): [Mastra](#mastra)

---

## Development & Debugging

### Sentry MCP Server

Integrates with Sentry's error tracking platform. Provides 19 tools including: find teams, find releases, get issue details, get trace details, create team, create project, and update project. Allows developers to search through issues, analyze them with Sentry's SEER AI platform, and manage Sentry projects directly from their code editor or CLI without switching to Sentry's web UI.

🔗 [GitHub](https://github.com/getsentry/sentry-mcp)

**CLI Installation:**
```bash
claude mcp add sentry -- npx -y @sentry/mcp-server@latest --access-token=YOUR_SENTRY_TOKEN
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "sentry": {
      "command": "npx",
      "args": ["-y", "@sentry/mcp-server@latest", "--access-token=YOUR_SENTRY_TOKEN"],
      "env": {
        "OPENAI_API_KEY": "YOUR_OPENAI_KEY"
      }
    }
  }
}
```

---

### SpotlightJS MCP Server

A local development debugging tool from Sentry (spotlightjs.com). Collects local errors, logs, and traces during development. Unlike the main Sentry MCP which is primarily for production bugs, SpotlightJS focuses on local debugging, allowing agents to access error information and logs without having to read console output or use Chrome DevTools.

🔗 [GitHub](https://github.com/getsentry/spotlight)

**CLI Installation:**
```bash
claude mcp add spotlight -- npx -y @spotlightjs/spotlight@latest mcp
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "spotlight": {
      "command": "npx",
      "args": ["-y", "@spotlightjs/spotlight@latest", "mcp"]
    }
  }
}
```

---

### Chrome DevTools MCP Server

The official MCP server from Chrome DevTools. Provides 26 tools including: emulate network, list console logs, click, drag, fill form, take screenshots, get performance metrics, and find animation issues/keyframe drops. Enables agents to test in the browser, find visual issues, and read console output directly.

🔗 [GitHub](https://github.com/anthropics/anthropic-quickstarts/tree/main/mcp-chrome-devtools)

**CLI Installation:**
```bash
claude mcp add chrome-devtools -- npx -y @anthropic-ai/mcp-server-chrome-devtools
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "chrome-devtools": {
      "command": "npx",
      "args": ["-y", "@anthropic-ai/mcp-server-chrome-devtools"],
      "env": {
        "CHROME_DEBUG_PORT": "9222"
      }
    }
  }
}
```

---

### Playwright MCP Server

A browser automation MCP server used for testing and interacting with web pages programmatically. Can take browser snapshots of your web app, grade them against UI/UX design standards, and create iterative self-correction loops where the AI generates output, reflects on it, and improves until the UI meets requirements.

🔗 [GitHub](https://github.com/microsoft/playwright-mcp)

**CLI Installation:**
```bash
claude mcp add playwright -- npx -y @playwright/mcp@latest
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["-y", "@playwright/mcp@latest"]
    }
  }
}
```

---

### Browser MCP

Allows AI to control your browser - clicking buttons, filling out forms, taking screenshots, and testing your app. Unlike Playwright which uses its own browser instance, Browser MCP uses your actual browser with all your cookies and logins already active. Can navigate to websites, read content, test local development servers, and read console errors.

🔗 [GitHub](https://github.com/BrowserMCP/mcp)

**CLI Installation:**
```bash
claude mcp add browser -- npx -y @browsermcp/mcp@latest
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "browser": {
      "command": "npx",
      "args": ["-y", "@browsermcp/mcp@latest"]
    }
  }
}
```

---

### Sequential Thinking MCP Server

Outsources complex thinking to an external thread, keeping your main AI context clean. Instead of wasting your AI's memory breaking down complex problems, it gives you the outcome of sequential thinking without consuming context. This leads to cleaner context, more focused AI, and better results. Completely free.

🔗 [GitHub](https://github.com/modelcontextprotocol/servers/tree/main/src/sequentialthinking)

**CLI Installation:**
```bash
claude mcp add sequential-thinking -- npx -y @modelcontextprotocol/server-sequential-thinking
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "sequential-thinking": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sequential-thinking"]
    }
  }
}
```

---

### Vibe Check MCP

A "metacognitive oversight layer" that prevents AI from overengineering or confidently following flawed plans. Uses a "chain pattern interrupt" system that injects brief pause points at risk inflection moments to realign the AI around user intent. Helps prevent "pattern inertia" and "reasoning lock in" where the AI snowballs into overly complex solutions.

🔗 [GitHub](https://github.com/PV-Bhat/vibe-check-mcp-server)

**CLI Installation:**
```bash
claude mcp add vibe-check -e GEMINI_API_KEY=YOUR_GEMINI_KEY -- npx -y @pv-bhat/vibe-check-mcp start --stdio
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "vibe-check": {
      "command": "npx",
      "args": ["-y", "@pv-bhat/vibe-check-mcp", "start", "--stdio"],
      "env": {
        "GEMINI_API_KEY": "YOUR_GEMINI_KEY"
      }
    }
  }
}
```

---

## Documentation & Research

### Context7 MCP Server

A documentation fetching tool that retrieves up-to-date documentation for various libraries and injects them into the AI's context. Maintains a vector database of documentation that is frequently updated and uses semantic search to retrieve relevant documentation snippets.

🔗 [GitHub](https://github.com/upstash/context7-mcp)

**CLI Installation:**
```bash
claude mcp add context7 -- npx -y @upstash/context7-mcp
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp"]
    }
  }
}
```

---

### Ref MCP Server

A context-efficient alternative to Context7 that combines multiple features including documentation, web search, web scraping, and code search on a single platform. Unlike Context7 which injects large documents into the context window, Ref exposes only the relevant parts using semantic search, reducing data pulled by up to 80%. Free tier includes 200 requests per month, then $9/month for additional 1,000 requests.

🔗 [GitHub](https://github.com/ref-tools/ref-tools-mcp)

**CLI Installation:**
```bash
claude mcp add ref -e REF_API_KEY=YOUR_API_KEY -- npx -y ref-tools-mcp@latest
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "ref": {
      "command": "npx",
      "args": ["-y", "ref-tools-mcp@latest"],
      "env": {
        "REF_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

---

### Perplexity MCP

Provides AI-powered research capabilities directly in your development workflow. Useful for researching new features (especially in unfamiliar areas), debugging problems by finding solutions from others who encountered similar issues, and understanding best practices for technologies you're not expert in.

🔗 [GitHub](https://github.com/ppl-ai/modelcontextprotocol)

**CLI Installation:**
```bash
claude mcp add perplexity -e PERPLEXITY_API_KEY=YOUR_API_KEY -- npx -y @perplexity-ai/mcp-server
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "perplexity": {
      "command": "npx",
      "args": ["-y", "@perplexity-ai/mcp-server"],
      "env": {
        "PERPLEXITY_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

---

## Framework-Specific

### Nuxt MCP Server

An MCP server specifically for working with Nuxt, created by AntFu. Available in the MCP registry on GitHub. This is a Nuxt module that provides MCP capabilities when your dev server runs.

🔗 [GitHub](https://github.com/antfu/nuxt-mcp)

**CLI Installation:**
```bash
# Install as Nuxt module in your project
npm install nuxt-mcp-dev
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "nuxt": {
      "type": "sse",
      "url": "http://localhost:3000/__mcp/sse"
    }
  }
}
```

---

### Svelte MCP Server

The official MCP server from the Svelte team (svelte.dev). Provides targeted documentation for Svelte 5 features and includes an "autofixer" tool that takes a component string, runs it through static analysis, and returns issues and suggestions for fixing Svelte-specific problems.

🔗 [GitHub](https://github.com/sveltejs/mcp)

**CLI Installation:**
```bash
claude mcp add svelte -e VOYAGE_API_KEY=YOUR_API_KEY -- npx -y @sveltejs/mcp
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "svelte": {
      "command": "npx",
      "args": ["-y", "@sveltejs/mcp"],
      "env": {
        "VOYAGE_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

---

### Flutter MCP

A Flutter plugin for building MCP-enabled Flutter apps. Supports STDIO, SSE, and StreamableHTTP transports. Cross-platform: Android, iOS, macOS, Windows, Linux, Web.

🔗 [GitHub](https://github.com/app-appplayer/flutter_mcp)

**CLI Installation:**
```bash
# Add to Flutter project
flutter pub add flutter_mcp
```

**JSON Configuration:**
```json
{
  "note": "Flutter MCP is a Flutter plugin, not a standalone MCP server. Add it to your Flutter project's pubspec.yaml",
  "pubspec.yaml": {
    "dependencies": {
      "flutter_mcp": "^1.0.5"
    }
  }
}
```

---

### Shadcn Registry MCP Server

Provides access to Shadcn UI components, a library of fully customizable UI components for web applications. Allows you to get components directly, install them, interact with items from Shadcn registries, and connect to custom registries like Aceternity UI and Magic UI.

🔗 [GitHub](https://github.com/heilgar/shadcn-ui-mcp-server)

**CLI Installation:**
```bash
claude mcp add shadcn -- npx -y @heilgar/shadcn-ui-mcp-server
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "shadcn": {
      "command": "npx",
      "args": ["-y", "@heilgar/shadcn-ui-mcp-server"]
    }
  }
}
```

---

## Cloud & Infrastructure

### Cloudflare MCP Servers

A collection of approximately 15 different MCP servers, one for each Cloudflare product. Includes servers for docs, APIs to spin up containers, create bindings to databases (like D1), and manage Wrangler bindings.

🔗 [GitHub](https://github.com/cloudflare/mcp-server-cloudflare)

**CLI Installation:**
```bash
# For Cloudflare Workers Bindings
claude mcp add cloudflare-bindings -- npx -y mcp-remote https://bindings.mcp.cloudflare.com/mcp

# For Cloudflare Documentation
claude mcp add cloudflare-docs -- npx -y mcp-remote https://docs.mcp.cloudflare.com/mcp
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "cloudflare-bindings": {
      "command": "npx",
      "args": ["-y", "mcp-remote", "https://bindings.mcp.cloudflare.com/mcp"]
    },
    "cloudflare-docs": {
      "command": "npx",
      "args": ["-y", "mcp-remote", "https://docs.mcp.cloudflare.com/mcp"]
    }
  }
}
```

---

### Vercel MCP Server

Puts your apps on the internet immediately. Key features include production debugging (seeing why deployments fail), live documentation access, and integration with Vercel's AI gateway. Has a generous free plan.

🔗 [GitHub](https://github.com/nganiet/mcp-vercel)

**CLI Installation:**
```bash
claude mcp add vercel -e VERCEL_API_TOKEN=YOUR_TOKEN -- node /path/to/mcp-vercel/dist/index.js
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "vercel": {
      "command": "node",
      "args": ["/path/to/mcp-vercel/dist/index.js"],
      "env": {
        "VERCEL_API_TOKEN": "YOUR_TOKEN"
      }
    }
  }
}
```

---

### Docker MCP

Acts as a bridge between all MCPs and helps with context saving. Uses two tools to let you connect with many MCPs directly within your AI agent. Key feature is reducing tools exposed in the context - only the tools required for the specific query are loaded. Docker maintains a catalog of verified MCP servers, and all tools run in a secure sandbox.

🔗 [GitHub](https://github.com/docker/mcp-gateway)

**CLI Installation:**
```bash
# Using Docker CLI plugin
docker mcp gateway run
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "docker": {
      "command": "uvx",
      "args": ["mcp-server-docker"]
    }
  }
}
```

---

### Kubernetes MCP

Simplifies container operations management. Native Go implementation with no external kubectl/helm dependencies.

🔗 [GitHub](https://github.com/containers/kubernetes-mcp-server)

**CLI Installation:**
```bash
claude mcp add kubernetes -- npx -y kubernetes-mcp-server@latest
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "kubernetes": {
      "command": "npx",
      "args": ["-y", "kubernetes-mcp-server@latest"]
    }
  }
}
```

---

## Google Services

### Google Maps MCP

A fully managed MCP server from Google that allows agents to use location-based grounding, pulling accurate data directly from Google Maps for AI agents.

🔗 [GitHub](https://github.com/cablate/mcp-google-map)

**CLI Installation:**
```bash
claude mcp add google-maps -- npx -y @cablate/mcp-google-map --port 3000 --apikey YOUR_GOOGLE_MAPS_API_KEY
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "google-maps": {
      "command": "npx",
      "args": ["-y", "@cablate/mcp-google-map", "--port", "3000", "--apikey", "YOUR_GOOGLE_MAPS_API_KEY"]
    }
  }
}
```

---

### BigQuery MCP

Enables agents to interpret enterprise data while eliminating issues of sensitive data in the context window.

🔗 [GitHub](https://github.com/LucasHild/mcp-server-bigquery)

**CLI Installation:**
```bash
claude mcp add bigquery -- uvx mcp-server-bigquery --project YOUR_PROJECT_ID --location YOUR_LOCATION
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "bigquery": {
      "command": "uvx",
      "args": ["mcp-server-bigquery", "--project", "YOUR_PROJECT_ID", "--location", "YOUR_LOCATION"]
    }
  }
}
```

---

### Google Compute MCP

Allows MCP to manage Google Cloud services.

🔗 *No official repository found - may require custom implementation using Google Cloud SDK*

**CLI Installation:**
```bash
# No official package available
# Consider using Google Cloud CLI directly or building a custom MCP server
```

**JSON Configuration:**
```json
{
  "note": "No official Google Compute MCP server available. Use Google Cloud CLI or custom implementation."
}
```

---

### Google Workspace MCP

Open-source MCP for Google Workspace services. Features Gmail, Google Calendar, Docs, Sheets, Slides, Chat, Forms, Tasks, Search, and Drive integration.

🔗 [GitHub](https://github.com/taylorwilsdon/google_workspace_mcp)

**CLI Installation:**
```bash
claude mcp add google-workspace -e GOOGLE_OAUTH_CLIENT_ID=YOUR_CLIENT_ID -e GOOGLE_OAUTH_CLIENT_SECRET=YOUR_SECRET -- uvx workspace-mcp
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "google-workspace": {
      "command": "uvx",
      "args": ["workspace-mcp"],
      "env": {
        "GOOGLE_OAUTH_CLIENT_ID": "YOUR_CLIENT_ID",
        "GOOGLE_OAUTH_CLIENT_SECRET": "YOUR_SECRET"
      }
    }
  }
}
```

---

### Google Analytics MCP

Open-source MCP for Google Analytics services. Access to 200+ GA4 dimensions and metrics through natural language queries.

🔗 [GitHub](https://github.com/surendranb/google-analytics-mcp)

**CLI Installation:**
```bash
claude mcp add google-analytics -e GOOGLE_APPLICATION_CREDENTIALS=/path/to/key.json -e GA4_PROPERTY_ID=YOUR_PROPERTY_ID -- python3 -m ga4_mcp_server
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "google-analytics": {
      "command": "python3",
      "args": ["-m", "ga4_mcp_server"],
      "env": {
        "GOOGLE_APPLICATION_CREDENTIALS": "/path/to/service-account-key.json",
        "GA4_PROPERTY_ID": "YOUR_PROPERTY_ID"
      }
    }
  }
}
```

---

## Database & Backend

### Supabase MCP Server

Handles all database and authentication needs. Can create tables, set up authentication, manage users, add fake users/data for testing, handle database schema management, and SQL operations. When something breaks, it tells you what broke, why it broke, and how to fix it. Can do security recommendations, see database logs, and find failed queries.

🔗 [GitHub](https://github.com/supabase-community/supabase-mcp)

**CLI Installation:**
```bash
claude mcp add supabase --transport http -- https://mcp.supabase.com/mcp
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "supabase": {
      "type": "http",
      "url": "https://mcp.supabase.com/mcp"
    }
  }
}
```

---

### Firebase MCP

Open-source MCP for Firebase services, frequently used for backend projects.

🔗 [GitHub](https://github.com/gannonh/firebase-mcp)

**CLI Installation:**
```bash
claude mcp add firebase -e SERVICE_ACCOUNT_KEY_PATH=/path/to/key.json -- npx -y @gannonh/firebase-mcp
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "firebase": {
      "command": "npx",
      "args": ["-y", "@gannonh/firebase-mcp"],
      "env": {
        "SERVICE_ACCOUNT_KEY_PATH": "/absolute/path/to/serviceAccountKey.json",
        "FIREBASE_STORAGE_BUCKET": "your-project-id.firebasestorage.app"
      }
    }
  }
}
```

---

## Payments & Business

### Stripe MCP Server

Provides access to the entire Stripe dashboard functionality. Tools include: create products, create customers, list customers, create prices, create invoices, finalize invoices, create coupons, set up subscriptions, handle refunds, and pull revenue data. The killer feature is debugging - it can help identify payment verification issues and provides accurate Stripe documentation.

🔗 [GitHub](https://github.com/stripe/agent-toolkit)

**CLI Installation:**
```bash
claude mcp add stripe -- npx -y @stripe/mcp --tools=all --api-key=YOUR_STRIPE_SECRET_KEY
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "stripe": {
      "command": "npx",
      "args": ["-y", "@stripe/mcp", "--tools=all", "--api-key=YOUR_STRIPE_SECRET_KEY"]
    }
  }
}
```

---

## Project Management & Productivity

### Linear MCP

Integrates Linear (a project management/issue tracking app) into your development workflow. Allows you to track issues, manage feature builds, add items to your backlog, and prioritize tasks directly from your coding environment.

🔗 [Linear MCP](https://mcp.linear.app)

**CLI Installation:**
```bash
claude mcp add linear --transport http -- https://mcp.linear.app/mcp
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "linear": {
      "type": "http",
      "url": "https://mcp.linear.app/mcp"
    }
  }
}
```

---

### GitHub MCP

Enables repository management, issue tracking, branching, and pull request automation directly from your coding environment. Helps with looking at commits across projects, creating issues, and automating pull request creation.

🔗 [GitHub](https://github.com/github/github-mcp-server)

**CLI Installation:**
```bash
claude mcp add github -e GITHUB_PERSONAL_ACCESS_TOKEN=YOUR_TOKEN -- docker run -i --rm -e GITHUB_PERSONAL_ACCESS_TOKEN ghcr.io/github/github-mcp-server
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "github": {
      "command": "docker",
      "args": ["run", "-i", "--rm", "-e", "GITHUB_PERSONAL_ACCESS_TOKEN", "ghcr.io/github/github-mcp-server"],
      "env": {
        "GITHUB_PERSONAL_ACCESS_TOKEN": "YOUR_TOKEN"
      }
    }
  }
}
```

---

### Notion MCP

Allows management of Notion pages including search, fetch, create, update, move, and various other tasks within connected workspaces. Useful for managing content, uploads, deadlines, research, and systems.

🔗 [GitHub](https://github.com/makenotion/notion-mcp-server)

**CLI Installation:**
```bash
claude mcp add notion -e NOTION_TOKEN=ntn_YOUR_TOKEN -- npx -y @notionhq/notion-mcp-server
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "notion": {
      "command": "npx",
      "args": ["-y", "@notionhq/notion-mcp-server"],
      "env": {
        "NOTION_TOKEN": "ntn_YOUR_TOKEN"
      }
    }
  }
}
```

---

### Obsidian MCP

Similar capabilities to Notion MCP but for Obsidian users. Can perform all the same operations and manage pages for those who prefer Obsidian over Notion.

🔗 [GitHub](https://github.com/smithery-ai/mcp-obsidian)

**CLI Installation:**
```bash
claude mcp add obsidian -- npx -y mcp-obsidian /path/to/your/vault
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "obsidian": {
      "command": "npx",
      "args": ["-y", "mcp-obsidian", "/path/to/your/vault"]
    }
  }
}
```

---

## Data & Web Scraping

### Apify MCP Server

A marketplace for web scrapers that turns your AI into a data gathering machine. Allows you to pull real-world data from websites (stock prices, news articles, YouTube comments, Instagram profiles, etc.). Provides access to full documentation of every web scraper on the platform, helps debug scrapers when things go wrong, and checks the status of recent jobs.

🔗 [GitHub](https://github.com/apify/actors-mcp-server)

**CLI Installation:**
```bash
claude mcp add apify -e APIFY_TOKEN=YOUR_TOKEN -- npx -y @apify/actors-mcp-server
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "apify": {
      "command": "npx",
      "args": ["-y", "@apify/actors-mcp-server"],
      "env": {
        "APIFY_TOKEN": "YOUR_TOKEN"
      }
    }
  }
}
```

---

## Security

### Semgrep MCP

Automates security vulnerability scanning in your codebase. Checks authentication handlers, server actions, middleware configuration, environment variable handling, and dependencies for security issues. Provides reports on vulnerabilities, their severity, and recommended actions.

🔗 [GitHub](https://github.com/semgrep/mcp)

**CLI Installation:**
```bash
claude mcp add semgrep -- uvx semgrep-mcp
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "semgrep": {
      "command": "uvx",
      "args": ["semgrep-mcp"],
      "env": {
        "SEMGREP_APP_TOKEN": "YOUR_TOKEN"
      }
    }
  }
}
```

---

## Voice & Communication

### 11 Labs MCP Server

An MCP server from 11 Labs (the voice/text-to-voice platform) that can integrate with their agents SDK. Enables features like making phone calls through agents, with responses being transcribed and fed back into the code editor.

🔗 [GitHub](https://github.com/elevenlabs/elevenlabs-mcp)

**CLI Installation:**
```bash
claude mcp add elevenlabs -e ELEVENLABS_API_KEY=YOUR_API_KEY -- uvx elevenlabs-mcp
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "elevenlabs": {
      "command": "uvx",
      "args": ["elevenlabs-mcp"],
      "env": {
        "ELEVENLABS_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

---

## Memory & Context

### Pieces MCP

Watches configured applications on your machine and forms memories around what you do. Processes everything locally using on-device machine learning. Allows you to search through past activities (like debugging sessions or configuration work) and have conversations about what solutions you found to previous problems.

🔗 [GitHub](https://github.com/pieces-app/pieces-os)

**CLI Installation:**
```bash
# Requires Pieces application with LTM engine enabled
# Build from source: https://github.com/jimbobbennett/PiecesMCPNet
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "pieces": {
      "command": "/path/to/PiecesMCPNet"
    }
  }
}
```

---

## Workflow & Orchestration

### Mastra

A platform/tool for building orchestration pipelines that allows developers to create and expose custom MCP servers. You can write custom tools in JavaScript (e.g., scraping pages, saving to SQLite databases), chain them together, and expose them as MCP servers. Includes a UI for testing, viewing results, and building parallel/branching workflows.

🔗 [GitHub](https://github.com/mastra-ai/mastra)

**CLI Installation:**
```bash
claude mcp add mastra -- npx -y @mastra/mcp-docs-server
```

**JSON Configuration:**
```json
{
  "mcpServers": {
    "mastra": {
      "command": "npx",
      "args": ["-y", "@mastra/mcp-docs-server"]
    }
  }
}
```

---

*Compiled from YouTube videos covering MCP servers for AI-assisted development.*
