# Claude Session Instructions

## Session Start Protocol

At the beginning of EVERY session, you MUST:

1. **Read the curriculum** to understand the learning framework:
   ```
   curriculum/prompt_engineering_curriculum.md
   ```

2. **Read progress files** to understand current state:
   ```
   progress/skills_tracker.md    # Current competency levels
   progress/session_log.md       # History of sessions
   progress/prompt_library.md    # Collected prompts
   ```

3. **Assess and suggest**:
   - Review which skills are marked "Not Started" or "In Progress"
   - Ask the user what they want to focus on today
   - OR suggest the next logical skill based on:
     - Prerequisites (foundation before advanced)
     - Skills marked "In Progress" that need completion
     - Natural progression through the curriculum

## During Session

- Follow the curriculum's output format for lessons:
  - Lesson Focus
  - Example Prompts (before/after optimization)
  - Key Takeaways
  - Debugging Notes
  - Mastery Checklist

- Always explain the **why** behind prompt decisions
- Encourage experimentation and iteration
- Prioritize teaching over producing

## Session End Protocol

At the end of EVERY session, you MUST:

### 1. Update Session Log
Append a new entry to `progress/session_log.md`:
```markdown
## Session [DATE]

**Focus Area:** [Topic covered]
**Duration:** [Approximate time]

### What We Covered
- [Bullet points of concepts/skills practiced]

### Key Insights
- [What worked, what didn't, principles learned]

### Prompts Developed
- [List any prompts created, with brief description]

### Next Session Recommendations
- [Suggested focus for next time]
```

### 2. Update Skills Tracker
Modify `progress/skills_tracker.md`:
- Change status from "Not Started" → "In Progress" → "Practiced" → "Competent" → "Mastered"
- Add notes on specific sub-skills covered
- Update last practiced date

### 3. Add to Prompt Library
For any successful prompts developed, add to `progress/prompt_library.md`:
```markdown
### [Prompt Name]
**Tags:** [use-case], [model], [technique]
**Effectiveness:** ⭐⭐⭐⭐⭐ (1-5)
**Created:** [DATE]

**Purpose:** [What this prompt accomplishes]

**The Prompt:**
```
[Actual prompt text]
```

**Why It Works:**
[Explanation of design choices]

**Variations:**
[Any alternate versions tested]
```

## Skill Progression Levels

| Level | Meaning |
|-------|---------|
| Not Started | Haven't covered this topic yet |
| In Progress | Currently learning, needs more practice |
| Practiced | Have worked through exercises, understand basics |
| Competent | Can apply independently with good results |
| Mastered | Can teach others, optimize for edge cases |

## Templates Reference

Use templates in `templates/` folder:
- `session_start.md` - Checklist for beginning sessions
- `session_wrap.md` - Template for ending sessions

## Important Reminders

- Never skip reading progress files at session start
- Always update progress files at session end
- Build on previous sessions - this is cumulative learning
- The prompt library is a valuable asset - maintain it carefully
