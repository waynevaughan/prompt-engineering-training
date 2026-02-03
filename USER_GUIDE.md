# Prompt Engineering Trainer - User Guide

A complete guide to using this self-contained learning environment for mastering prompt engineering.

---

## Table of Contents

1. [Getting Started](#getting-started)
2. [Starting a Learning Session](#starting-a-learning-session)
3. [During Your Session](#during-your-session)
4. [Ending a Session](#ending-a-session)
5. [Understanding Your Progress](#understanding-your-progress)
6. [Building Your Prompt Library](#building-your-prompt-library)
7. [Practice Exercises](#practice-exercises)
8. [Tips for Effective Learning](#tips-for-effective-learning)
9. [Troubleshooting](#troubleshooting)

---

## Getting Started

### Prerequisites

- An AI assistant that can read files (Claude Code, Cursor, or similar)
- This repository cloned locally or accessible to your AI tool

### First-Time Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/waynevaughan/prompt-engineering-training.git
   cd prompt-engineering-training
   ```

2. **Open in your AI-enabled editor** (Claude Code, Cursor, etc.)

3. **Start your first session** by telling the AI:
   > "Let's start my prompt engineering training."

The AI will automatically read `CLAUDE.md` and follow the session protocols.

---

## Starting a Learning Session

### What Happens Automatically

When you begin a session, the AI will:

1. **Read the curriculum** to understand the learning framework
2. **Check your progress** by reading:
   - `progress/skills_tracker.md` - your current skill levels
   - `progress/session_log.md` - what you covered previously
   - `progress/prompt_library.md` - prompts you've developed
3. **Suggest what to focus on** based on your progress

### Ways to Start

**Option 1: Let the AI guide you**
> "Let's continue my prompt engineering training."

The AI will suggest the next logical skill based on your tracker.

**Option 2: Request a specific topic**
> "I want to learn about XML block structuring for prompts."

**Option 3: Work on a real task**
> "I need to write a prompt for summarizing research papers. Can we use that as practice?"

**Option 4: Review and consolidate**
> "Let's review what I've learned about role framing before moving on."

---

## During Your Session

### Lesson Structure

Each lesson follows this format:

```
### Lesson Focus
The concept or skill being taught

### Example Prompts
Before and after optimization, with annotations

### Key Takeaways
Core principles demonstrated

### Debugging Notes
Common pitfalls and how to avoid them

### Mastery Checklist
Skills to verify understanding
```

### Active Learning Techniques

**Ask "why" questions:**
> "Why did adding the role framing improve the output?"

**Request variations:**
> "Show me how this prompt would change for ChatGPT vs Claude."

**Try modifications:**
> "What if I removed the format constraints? Let me test it."

**Debug together:**
> "This prompt isn't giving me what I want. Can we analyze why?"

### Taking Notes

Use the session templates in `templates/` or take notes directly in the chat. The AI will help compile important points at session end.

---

## Ending a Session

### Wrap-Up Process

When you're ready to end, say:
> "Let's wrap up this session."

The AI will:

1. **Summarize what you covered**
2. **Update the session log** - append an entry to `progress/session_log.md`
3. **Update your skills** - modify statuses in `progress/skills_tracker.md`
4. **Add new prompts** - save successful prompts to `progress/prompt_library.md`
5. **Recommend next steps** - suggest what to focus on next time

### What Gets Recorded

**Session Log Entry:**
```markdown
## Session 2025-02-02

**Focus Area:** Role framing techniques
**Duration:** 45 minutes

### What We Covered
- Persona-based role framing
- Expertise level specification
- Combining roles for complex tasks

### Key Insights
- Specific expertise beats generic roles
- Role + goal alignment produces better outputs

### Prompts Developed
- Research analyst prompt for literature review

### Next Session Recommendations
- Move to constraint definition techniques
```

### Committing Your Progress (Optional)

After a session, you can commit changes:
```bash
git add progress/
git commit -m "Session: [topic covered]"
git push
```

---

## Understanding Your Progress

### The Skills Tracker

Located at `progress/skills_tracker.md`, this tracks 54 skills across 8 sections.

**Skill Levels:**

| Symbol | Level | Meaning |
|--------|-------|---------|
| ⬜ | Not Started | Haven't covered yet |
| 🟡 | In Progress | Currently learning |
| 🟠 | Practiced | Understand basics |
| 🟢 | Competent | Can apply independently |
| ⭐ | Mastered | Can teach others |

**Example Tracker Entry:**
```markdown
## Section 2: Prompt Architecture

**Overall Status:** 🟡 In Progress
**Last Practiced:** 2025-02-02

### Sub-Skills

| Skill | Status | Notes |
|-------|--------|-------|
| Role framing techniques | 🟠 Practiced | Good with personas |
| Goal specification clarity | 🟡 In Progress | Need more practice |
| Constraint definition | ⬜ Not Started | |
```

### Reading Your Dashboard

At the bottom of `skills_tracker.md`:

```markdown
## Summary Dashboard

| Section | Status | Progress |
|---------|--------|----------|
| 1. Foundation Building | 🟠 Practiced | 4/6 |
| 2. Prompt Architecture | 🟡 In Progress | 2/8 |
| 3. Applied Practice | ⬜ Not Started | 0/7 |
...

**Total Sub-Skills:** 6/54 started
```

### Recommended Progression Path

```
1. Foundation Building     ─┐
                            ├─► 3. Applied Practice
2. Prompt Architecture     ─┘
                                      │
4. Debugging & Optimization ◄─────────┘
         │
         ▼
5. System Design Thinking
         │
         ▼
6. Documentation & Mastery
         │
         ├─► 7. Cross-Model Expertise
         │
         └─► 8. Advanced Techniques
```

---

## Building Your Prompt Library

### Why Keep a Library?

- **Reuse** proven prompts instead of starting from scratch
- **Track** what works and what doesn't
- **Learn** from patterns across your successful prompts
- **Share** techniques with others

### Library Structure

Located at `progress/prompt_library.md`:

```markdown
### Research Paper Summarizer

**Tags:** #research, #claude, #structured, #chain-of-thought
**Effectiveness:** ⭐⭐⭐⭐
**Created:** 2025-02-02

**Purpose:**
Summarize academic papers with key findings, methodology, and relevance.

**The Prompt:**
```
You are a research analyst specializing in [field].

Read the following paper and provide:
1. Core thesis (1-2 sentences)
2. Methodology summary
3. Key findings (bullet points)
4. Limitations noted
5. Relevance to [specific context]

Paper: [content]
```

**Why It Works:**
- Role framing establishes expertise
- Numbered structure ensures completeness
- Customization points for field and context

**Variations Tested:**
- Without role framing: Less technical depth
- Without numbered list: Inconsistent coverage
```

### Tagging System

**Use Case Tags:**
- `#research` - Information gathering
- `#creative` - Writing and content
- `#analysis` - Data interpretation
- `#coding` - Code generation
- `#decision` - Decision support
- `#teaching` - Explanation

**Model Tags:**
- `#claude`, `#chatgpt`, `#gemini`, `#grok`, `#perplexity`, `#universal`

**Technique Tags:**
- `#role-framing`, `#structured`, `#chain-of-thought`, `#few-shot`, `#zero-shot`

### Adding Prompts During Sessions

When you develop a good prompt, tell the AI:
> "This prompt worked well. Let's add it to my library."

The AI will help you:
- Choose appropriate tags
- Rate effectiveness
- Document why it works
- Note any variations tested

---

## Practice Exercises

### Exercise Folder Structure

```
practice/
├── 01-foundation/        # Core principles
├── 02-architecture/      # Structural techniques
├── 03-applied/           # Domain-specific tasks
├── 04-debugging/         # Optimization challenges
├── 05-systems/           # Workflow design
├── 06-documentation/     # Library building
├── 07-cross-model/       # Model comparison
└── 08-advanced/          # Complex techniques
```

### Types of Exercises

**Improvement exercises:**
> "Here's a basic prompt. Make it better."

**Debugging exercises:**
> "This prompt produces inconsistent results. Fix it."

**Translation exercises:**
> "Adapt this Claude prompt for ChatGPT."

**Real-world challenges:**
> "Write a prompt for [your actual use case]."

### Creating Custom Exercises

Add your own based on real needs:

```markdown
# Exercise: [Your Task]

## Objective
What skill this develops

## Task
The specific challenge

## Your Attempts
1. First try: [prompt]
   Result: [what happened]

2. Refined: [improved prompt]
   Result: [what changed]

## What I Learned
[Key insight]
```

---

## Tips for Effective Learning

### 1. Be Consistent
Short regular sessions beat long sporadic ones. Aim for 20-30 minutes, 2-3 times per week.

### 2. Learn by Doing
Don't just read about techniques—try them immediately with real tasks.

### 3. Embrace Failure
Bad outputs teach more than good ones. When a prompt fails, dig into why.

### 4. Document Everything
Your prompt library becomes increasingly valuable over time. Don't skip documentation.

### 5. Test Across Models
A prompt that works on Claude may fail on ChatGPT. Understanding differences builds real expertise.

### 6. Iterate Aggressively
Never stop at your first attempt. Try 3-5 variations of every prompt.

### 7. Explain Back
After learning a concept, try explaining it to the AI. Teaching solidifies understanding.

### 8. Connect to Real Work
Apply new techniques to actual tasks you face. Abstract learning doesn't stick.

---

## Troubleshooting

### "The AI didn't read my progress files"

Remind it explicitly:
> "Please read CLAUDE.md and follow the session start protocol."

### "My skills aren't being tracked"

At session end, explicitly request:
> "Update my skills_tracker.md with what we covered today."

### "I'm not sure what to learn next"

Ask for assessment:
> "Based on my skills tracker, what should I focus on and why?"

### "The lessons feel too basic/advanced"

Calibrate the level:
> "I already know the basics of role framing. Let's go deeper into edge cases."
> "This is too advanced. Can we back up and cover prerequisites?"

### "I want to focus on a specific model"

Request model-specific training:
> "I primarily use ChatGPT. Let's focus on techniques that work best there."

### "How do I know when I've mastered a skill?"

Mastery criteria:
- Can apply the technique without guidance
- Can explain why it works to someone else
- Can debug when it fails
- Can adapt it to new situations

---

## Quick Reference

### Session Commands

| Say This | To Do This |
|----------|------------|
| "Let's start training" | Begin with AI-guided topic |
| "I want to learn [topic]" | Request specific focus |
| "Let's practice with [task]" | Apply to real work |
| "Why did that work?" | Get explanation |
| "Show me variations" | See alternatives |
| "Let's wrap up" | End and document session |
| "Add this to my library" | Save successful prompt |

### File Locations

| File | Purpose |
|------|---------|
| `CLAUDE.md` | AI instructions |
| `curriculum/prompt_engineering_curriculum.md` | Learning framework |
| `progress/skills_tracker.md` | Your competency matrix |
| `progress/session_log.md` | Session history |
| `progress/prompt_library.md` | Your prompt collection |
| `templates/session_start.md` | Session opening checklist |
| `templates/session_wrap.md` | Session closing template |

---

## Getting Help

If you're stuck or have questions about using the trainer:

1. Ask the AI directly—it has full context of the system
2. Review `CLAUDE.md` for session protocols
3. Check `curriculum/prompt_engineering_curriculum.md` for learning objectives

Happy learning!
