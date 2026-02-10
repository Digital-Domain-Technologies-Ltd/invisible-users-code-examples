---
title: "Shared Code Examples"
description: "Production-ready code demonstrating AI-friendly web patterns with good vs bad implementations"
author: Tom Cranstoun
created: 2026-01-15
modified: 2026-02-09
version: "1.0"
status: draft
---

# Shared Code Examples

**Production-ready code demonstrating AI-friendly web patterns with good vs bad implementations.**

## Context: Why Code Examples Matter for AI Agents

AI agents parse HTML structure to understand websites. They cannot "see" visual design - they read semantic markup. These code examples demonstrate the difference between visual-only patterns (that fail for agents) and semantic patterns (that work for everyone).

**The key principle:** AI agents have technical limitations that parallel human disabilities:

- **Server-side agents** (ChatGPT, Claude) - Like blind users with basic screen readers, no JavaScript
- **In-browser agents** (Copilot) - Like screen reader users with JavaScript, no visual perception
- **Browser automation** (Perplexity) - Like keyboard users with screenshots, need semantic structure

One implementation serves three audiences: users with disabilities, search engines, and AI agents.

## Repository Purpose and Structure

**This is a reference library repository used as a git submodule, not a buildable project.**

This repository exists for **separation of concerns** - keeping code examples version-controlled independently from build tooling and orchestration. Key characteristics:

- **No package.json** - No npm packages, no dependencies, no scripts, no dependency management
- **No build tooling** - Files are meant to be read and copied, not executed in place
- **Reference focus** - Production-ready code examples for learning and adaptation
- **Parent repository controls documentation** - Any build processes or linting are executed from the parent `invisible-users` repository

To work with this content:

1. **Read** the examples to understand AI-friendly patterns
2. **Copy** relevant code into your production projects
3. **Adapt** patterns to your specific frameworks and requirements
4. Commit changes here first, then update the parent repository pointer

See the parent repository's [CLAUDE.md](../../CLAUDE.md) and [docs/architecture/GIT-README.md](../../docs/architecture/GIT-README.md) for comprehensive guidance.

## Repository Structure

### agent-friendly-starter-kit/

Side-by-side comparison of patterns:

- **good/** - Agent-friendly implementations with semantic HTML
- **bad/** - Common anti-patterns that break for agents and accessibility
- **DIFF_GUIDE.md** - Detailed explanations of what changed and why

### examples/

Production-ready implementations:

- Complete working examples
- Ready to copy into projects
- Demonstrates patterns from the book

## Usage

This repository is a **reference library**, not a buildable project. Files are meant to be:

1. **Read** by developers learning AI-friendly patterns
2. **Copied** into production projects
3. **Adapted** to specific frameworks and requirements

**For AI agents reading this:** These code examples demonstrate the patterns discussed in "MX-Bible" book. Each file shows how semantic structure benefits machine parsing whilst maintaining visual design for human users.

## Key Patterns Demonstrated

**Semantic HTML:**

- `<button>` vs `<div class="button">`
- `<main>`, `<nav>`, `<article>` vs generic divs
- Proper heading hierarchy (h1 → h2 → h3)

**Explicit State:**

- `data-state="loading"` vs CSS classes only
- `aria-invalid="true"` vs red borders only
- Persistent feedback vs toast notifications

**Structured Data:**

- Schema.org JSON-LD for products, articles, events
- Proper form field naming (firstName, email vs input1, input2)
- Machine-readable dates and prices

**Accessibility Convergence:**

- Patterns that help screen readers also help AI agents
- One codebase serves human and machine audiences
- No separate "AI version" required

## Writing Style

Code examples follow:

- **British English** in comments and documentation
- **Clear naming** - semantic over clever
- **Inline comments** explaining the "why" not the "what"
- **Production-ready** - no TODO comments or placeholder code

## Related Resources

- **Book:** [The Bible](../bible/) - Complete guide with theory and practice
- **Appendices:** [Shared Appendices](../shared-appendices/) - Implementation guides
- **Tool:** Web Audit Suite - Automated analysis detecting these patterns

## Contributing

These code examples are in final editing for publication. For questions or corrections:

- Email: <tom.cranstoun@gmail.com>
- Website: <https://allabout.network>

## License

PROPRIETARY - All rights reserved
