# Claude Skills List

A comprehensive list of community-built Claude Skills and Hooks compiled from Reddit and GitHub.

---

## Table of Contents

- **[Essential Skills](#essential-skills)** (3): [Superpowers](#superpowers), [Superpowers Lab](#superpowers-lab), [Skill Seekers](#skill-seekers)
- **[Developer Workflow](#developer-workflow)** (8): [Test-Driven Development](#test-driven-development-skill), [Systematic Debugging](#systematic-debugging-skill), [Finishing a Development Branch](#finishing-a-development-branch-skill), [Using Git Worktrees](#using-git-worktrees-skill), [Pypict](#pypict-skill), [Webapp Testing with Playwright](#webapp-testing-with-playwright-skill), [ffuf Security Fuzzing](#ffuf-security-fuzzing-skill), [Defense-in-Depth](#defense-in-depth-skill)
- **[Research & Knowledge](#research--knowledge)** (5): [Tapestry](#tapestry), [YouTube/Article Extractor](#youtubearticle-extractor-skills), [Brainstorming](#brainstorming-skill), [Content Research Writer](#content-research-writer-skill), [EPUB & PDF Analyzer](#epub--pdf-analyzer)
- **[Productivity & Automation](#productivity--automation)** (2): [Invoice/File Organizer](#invoicefile-organizer-skills), [Web Asset Generator](#web-asset-generator-skill)
- **[Claude Code Hooks](#claude-code-hooks)** (8): [claude-hooks (TypeScript)](#claude-hooks-typescript), [CCHooks (Python)](#cchooks-python), [claude-code-hooks-sdk (PHP)](#claude-code-hooks-sdk-php), [Claudio](#claudio), [CC Notify](#cc-notify), [claude-code-discord](#claude-code-discord), [fcakyon Code Quality](#fcakyon-code-quality-collection), [TypeScript Quality Hooks](#typescript-quality-hooks)

---

## Essential Skills

### Superpowers

The Swiss Army knife of Claude Skills. Provides brainstorming, debugging, TDD enforcement, and execution planning - all with slash commands. The `/superpowers:execute-plan` command helps automate multi-step workflows. Takes a day or two to learn but becomes indispensable.

🔗 [GitHub](https://github.com/obra/superpowers)

**Installation:**
```bash
/plugin marketplace add obra/superpowers-marketplace
/plugin install superpowers@superpowers-marketplace
```

---

### Superpowers Lab

Experimental/bleeding-edge version of Superpowers. For those who want to try new features before they're stable. Use this if you want to live on the cutting edge.

🔗 [GitHub](https://github.com/obra/superpowers-lab)

**Installation:**
```bash
/plugin marketplace add obra/superpowers-lab-marketplace
/plugin install superpowers-lab@superpowers-lab-marketplace
```

---

### Skill Seekers

Point it at ANY documentation site, PDF, or codebase and it auto-generates a Claude Skill. Perfect for internal frameworks or tools that Claude knows nothing about. Works with React docs, Django docs, Godot, or any custom documentation.

🔗 [GitHub](https://github.com/yusufkaraaslan/Skill_Seekers)

**Installation:**
Follow the instructions in the GitHub repository to set up the skill generator.

---

## Developer Workflow

### Test-Driven Development Skill

Enforces actual TDD workflows. Makes Claude write tests first, not as an afterthought. Helps maintain discipline in test-first development practices.

🔗 [GitHub](https://github.com/obra/superpowers) | [Awesome Claude Skills](https://github.com/BehiSecc/awesome-claude-skills)

**Installation:**
Included in Superpowers or available separately from awesome-claude-skills repository.

---

### Systematic Debugging Skill

Stops Claude from just guessing at fixes. Forces root-cause analysis like an experienced developer would approach debugging. Actually finds issues instead of throwing random fixes at problems.

🔗 [GitHub](https://github.com/obra/superpowers)

**Installation:**
Included in Superpowers skill pack.

---

### Finishing a Development Branch Skill

Streamlines the "merge, clean up, and finalize" workflow when finishing work on a branch. Automates the tedious end-of-branch tasks.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repository.

---

### Using Git Worktrees Skill

Essential for developers working on multiple branches simultaneously. Makes Claude actually understand and work effectively with git worktrees.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repository.

---

### Pypict Skill

Generates combinatorial testing cases. For robust QA when you need comprehensive test coverage without manually writing hundreds of test cases.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repository.

---

### Webapp Testing with Playwright Skill

Automates web app testing. Claude can test your UI flows end-to-end using Playwright automation.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repository.

---

### ffuf Security Fuzzing Skill

Security fuzzing and vulnerability analysis tool. Essential for any security testing work.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repository.

---

### Defense-in-Depth Skill

Multi-layered security and quality checks for your codebase. Hardens your code with comprehensive security practices.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repository.

---

## Research & Knowledge

### Tapestry

Takes technical docs and creates a navigable knowledge graph. Turn 50+ API PDFs into an interconnected wiki you can actually query.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills) | [Alternative](https://github.com/travisvn/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repositories.

---

### YouTube/Article Extractor Skills

Scrapes and summarizes YouTube videos or web articles. Great for research without watching 50 hours of content.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repository.

---

### Brainstorming Skill

Turns rough ideas into structured design plans. Transforms vague thoughts into actionable plans.

🔗 [GitHub](https://github.com/obra/superpowers)

**Installation:**
Included in Superpowers skill pack.

---

### Content Research Writer Skill

Adds citations, iterates on quality, and organizes research automatically. Essential for writing content backed by research.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repository.

---

### EPUB & PDF Analyzer

Summarizes or queries ebooks and academic papers. Popular with academic researchers.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repository.

---

## Productivity & Automation

### Invoice/File Organizer Skills

Smart categorization for receipts, documents, and finance files. Point it at a folder of chaos and get structure back. Tax season life-saver.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repository.

---

### Web Asset Generator Skill

Auto-creates icons, Open Graph tags, and PWA assets. Saves web developers about an hour per project.

🔗 [GitHub](https://github.com/BehiSecc/awesome-claude-skills) | [Alternative](https://github.com/travisvn/awesome-claude-skills)

**Installation:**
Available from the awesome-claude-skills repositories.

---

## Claude Code Hooks

Hooks are event-driven triggers for Claude Code. When Claude does something, your hook runs. Super powerful for automation.

### claude-hooks (TypeScript)

The main hooks framework. TypeScript with auto-completion and typed payloads. Foundation for anything programmatic with Claude Code. Requires TypeScript knowledge.

🔗 [GitHub](https://github.com/johnlindquist/claude-hooks)

**Installation:**
```bash
git clone https://github.com/johnlindquist/claude-hooks
cd claude-hooks
npm install
```

---

### CCHooks (Python)

Python version of Claude hooks. Minimal, clean abstraction. Great for those who prefer Python over TypeScript.

🔗 [GitHub](https://github.com/hesreallyhim/awesome-claude-code) (search for GowayLee CCHooks)

**Installation:**
Follow installation instructions in the awesome-claude-code repository.

---

### claude-code-hooks-sdk (PHP)

PHP/Laravel-style hooks for the PHP community.

🔗 [GitHub](https://github.com/hesreallyhim/awesome-claude-code) (search for beyondcode claude-code-hooks)

**Installation:**
Follow installation instructions in the awesome-claude-code repository.

---

### Claudio

Adds OS-native sounds to Claude. Beep when Claude finishes a task, ding when errors happen. Sounds silly but weirdly satisfying.

🔗 [GitHub](https://github.com/hesreallyhim/awesome-claude-code) (search for Christopher Toth Claudio)

**Installation:**
Follow installation instructions in the awesome-claude-code repository.

---

### CC Notify

Desktop notifications, session reminders, and progress alerts. Know when Claude finishes long tasks while you're in another window.

🔗 [GitHub](https://github.com/hesreallyhim/awesome-claude-code)

**Installation:**
Available from the awesome-claude-code repository.

---

### claude-code-discord

Real-time session activity notifications to Discord or Slack. Great for teams or keeping a log of Claude's activity.

🔗 [GitHub](https://github.com/codeinbox/claude-code-discord)

**Installation:**
```bash
git clone https://github.com/codeinbox/claude-code-discord
cd claude-code-discord
npm install
```

---

### fcakyon Code Quality Collection

Various code quality hooks including TDD enforcement, linting, and tool checks. Comprehensive solution for enforcing standards across team Claude usage.

🔗 [GitHub](https://github.com/hesreallyhim/awesome-claude-code) (search for fcakyon)

**Installation:**
Follow installation instructions in the awesome-claude-code repository.

---

### TypeScript Quality Hooks

Advanced project health for TypeScript projects. Instant validation and format-fixers. Catches TypeScript issues before they become problems.

🔗 [GitHub](https://github.com/hesreallyhim/awesome-claude-code) (search for bartolli)

**Installation:**
Follow installation instructions in the awesome-claude-code repository.

---

## Resource Hubs

Main repositories for discovering more skills and hooks:

- **Skills:** [BehiSecc/awesome-claude-skills](https://github.com/BehiSecc/awesome-claude-skills)
- **Skills:** [travisvn/awesome-claude-skills](https://github.com/travisvn/awesome-claude-skills)
- **Hooks:** [hesreallyhim/awesome-claude-code](https://github.com/hesreallyhim/awesome-claude-code)

---

## Recommendations by Use Case

**For Developers:**
1. Get Superpowers + Systematic Debugging immediately
2. Try TDD Skill and Git Worktrees Skill
3. Learn johnlindquist/claude-hooks if you use Claude Code
4. Explore fcakyon's quality hooks for code standards

**For Researchers/Writers:**
1. Tapestry for knowledge management
2. Content Research Writer for citations
3. YouTube/Article Extractors for quick research
4. EPUB/PDF Analyzer for academic work

**For Claude Code Users:**
1. johnlindquist/claude-hooks as foundation
2. CC Notify for task completion alerts
3. fcakyon Code Quality Collection for standards
4. Claudio for fun sound effects

---

*Compiled from community contributions on Reddit and GitHub.*
