# 🚀 pm-workspace-template

> A modern, AI-powered workspace for product managers

Complete PM toolkit with templates, automation, and Claude Code integration for a **Terminal + Cursor** workflow. Stop reinventing your PRDs, roadmaps, and status updates — start with a proven structure and let AI handle the heavy lifting.

---

## 📋 Overview

**pm-workspace-template** is a reusable foundation for product management work. It provides:

- **Ready-to-use templates** for PRDs, roadmaps, status updates, research docs, decision logs, and metrics definitions
- **Prioritization & discovery frameworks** you can apply immediately
- **Automation scripts** to eliminate repetitive PM tasks
- **Deep Claude Code integration** so AI understands your PM context, preferences, and writing style

### Why does this exist?

Every PM builds their own system from scratch — folder structures, templates, checklists, communication formats. This template captures best practices into a portable, version-controlled workspace that works with modern AI tooling. Clone it once, customize it to your style, and reuse it across every product you manage.

---

## ✨ Key Features

### 📝 Templates
Battle-tested templates for every core PM artifact — PRDs, roadmaps, weekly updates, research briefs, decision documents, and metrics definitions. Each template includes guidance on when and how to use it.

### ⚡ Automation
Scripts to generate documents, compile status updates, track metrics, and streamline repetitive workflows. Built for the command line so they integrate naturally with your dev environment.

### 🤖 Claude Code Integration
A `.claude/` directory with PM-specific preferences and prompts. Claude learns your writing style, document standards, and process — so every AI-assisted draft already sounds like you.

### 🎨 Communication Styles
Built-in support for tailoring documents to different audiences — engineering, leadership, design, customers — with configurable tone and detail levels.

### 📊 Frameworks
Prioritization models (RICE, MoSCoW, Impact/Effort) and discovery frameworks (Opportunity Solution Trees, Jobs-to-be-Done) ready to apply to your product decisions.

---

## 🏗️ Two-Layer Architecture

This workspace uses a simple but powerful two-layer model:

```
Layer 1: pm-workspace-template (this repo)
├── Your reusable foundation
├── Templates, frameworks, automation, styles
├── PM preferences & Claude Code config
└── Doesn't change per product
```

```
Layer 2: project folders (created per product)
├── your-product/
│   ├── prds/           ← Product-specific PRDs
│   ├── roadmap/        ← This product's roadmap
│   ├── research/       ← User research & findings
│   ├── decisions/      ← Decision log
│   └── metrics/        ← KPIs & dashboards
└── another-product/
    └── ...
```

**Layer 1** = your reusable toolkit. Clone once, customize, keep forever.
**Layer 2** = product-specific work. Create a folder per product, fill it using Layer 1 templates.

This separation means your standards, preferences, and tools travel with you — even when you change teams, companies, or products.

---

## 🚀 Quick Start

### 1. Clone the template
```bash
git clone https://github.com/your-username/pm-workspace-template.git
cd pm-workspace-template
```

### 2. Personalize your preferences
```bash
# Open and customize your PM preferences
# Claude Code reads this to match your style
code .claude/pm-preferences.md
```

### 3. Start using templates
```bash
# Copy a template to start a new PRD
cp templates/prds/prd-template.md my-project/prds/feature-x.md

# Or let Claude help you draft one
claude "Draft a PRD for [your feature] using the PRD template"
```

### 4. Create a project folder
```bash
mkdir -p my-product/{prds,roadmap,research,decisions,metrics}
```

---

## 📁 Directory Structure

```
pm-workspace-template/
│
├── 📝 templates/               # Reusable document templates
│   ├── prds/                   #   Product Requirements Documents
│   ├── roadmaps/               #   Roadmap formats
│   ├── updates/                #   Status update templates
│   ├── research/               #   Research brief templates
│   ├── decisions/              #   Decision document templates
│   └── metrics/                #   Metrics definition templates
│
├── 🧠 frameworks/              # PM frameworks & models
│   ├── prioritization/         #   RICE, MoSCoW, Impact/Effort
│   ├── discovery/              #   OST, JTBD, user research
│   └── metrics/                #   North Star, KPI trees, funnels
│
├── ⚡ automation/               # Workflow automation
│
├── 🔧 scripts/                 # Utility scripts
│
├── 🤖 .claude/                 # Claude Code configuration
│   ├── pm-preferences.md       #   Your personal PM preferences
│   └── prompts/                #   Reusable prompt templates
│
├── 🎨 styles/                  # Communication style guides
│
├── 📚 examples/                # Example documents
│   ├── prds/                   #   Example PRDs
│   ├── roadmaps/               #   Example roadmaps
│   └── updates/                #   Example status updates
│
├── 📖 docs/                    # Documentation
│
├── .gitignore
├── LICENSE
└── README.md
```

---

## 💡 Usage Examples

### Terminal + Claude Code

```bash
# Draft a PRD from a one-liner
claude "Write a PRD for adding dark mode to our mobile app.
       Target: iOS first, Q2 launch. Use the PRD template."

# Generate a weekly status update
claude "Write my weekly status update.
       Wins: shipped search v2, closed 3 bugs.
       Risks: API rate limits on partner integration.
       Asks: need design review for onboarding flow."

# Prioritize a feature backlog
claude "Here are 10 feature requests from customers.
       Score them using RICE and recommend the top 3 for next quarter."

# Translate a PRD for different audiences
claude "Take this PRD and create an executive summary for leadership
       and a technical brief for the engineering team."
```

### Cursor Integration

Open the workspace in Cursor for a visual editing experience with AI assistance:

```bash
cursor .
```

- Use Cursor's AI chat to iterate on documents with full workspace context
- Templates auto-complete when you reference them in chat
- Claude Code preferences carry over — your style stays consistent

### Combined Workflow

```bash
# 1. Research in terminal
claude "Summarize the latest trends in AI-powered search for e-commerce"

# 2. Draft in terminal
claude "Draft a PRD for adding AI search to our platform"

# 3. Refine in Cursor
cursor my-product/prds/ai-search.md

# 4. Generate stakeholder versions in terminal
claude "Create an exec summary and eng spec from this PRD"
```

---

## 🔧 Customization

### Personalizing Templates
Every template is a starting point. Modify them to match your team's standards:

```bash
# Edit any template directly
code templates/prds/prd-template.md
```

### Setting Your Preferences
Your `.claude/pm-preferences.md` file controls how Claude assists you:

- **Communication styles** — how to write for different audiences
- **Document standards** — what to always include (or exclude)
- **Writing voice** — your tone, favorite phrases, words to avoid
- **Process** — how you approach discovery, prioritization, shipping
- **Review checklist** — your quality bar before sharing docs

### Adding Custom Prompts
Create reusable prompts in `.claude/prompts/` for tasks you repeat often:

```bash
# Example: a prompt for competitive analysis
echo "Analyze [competitor] across these dimensions: ..." > .claude/prompts/competitive-analysis.md
```

### Adding Frameworks
Drop new frameworks into `frameworks/` and they become part of your toolkit:

```
frameworks/
├── prioritization/
│   ├── rice-scoring.md
│   └── moscow-method.md
├── discovery/
│   ├── opportunity-solution-tree.md
│   └── jobs-to-be-done.md
└── metrics/
    ├── north-star-framework.md
    └── kpi-tree.md
```

---

## 🤝 Contributing

Contributions are welcome! This template improves when PMs share what works.

### How to contribute
1. **Fork** the repository
2. **Create a branch** for your addition (`git checkout -b add-sprint-review-template`)
3. **Add your contribution** — templates, frameworks, scripts, or improvements
4. **Submit a pull request** with a clear description of what you added and why

### What we're looking for
- New templates for common PM artifacts
- Frameworks and models that PMs use regularly
- Automation scripts that save time
- Improvements to existing templates based on real-world usage
- Documentation and examples

### Guidelines
- Keep templates generalizable — avoid company-specific details
- Include usage instructions in every template
- Test automation scripts before submitting
- Follow the existing directory structure

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

Use it, customize it, share it. Build something great. 🎯
