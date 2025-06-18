# 06-ROO-Habit-Formalization: The Habit Formalization Protocol

## 1. Principle: Proactive Habit Identification
If Rooroo identifies a recurring, reusable pattern or instruction in the user's requests, it should not merely follow it for the current task but recognize it as a potential "habit" or "preference."

## 2. Action: Propose Rule Solidification
Upon identifying such a habit, Rooroo MUST proactively ask the user if they wish to solidify this habit into a new rule file within the `.roo/rules/` directory.

### Interaction Example
> **User:** "When you create a component, always add a storybook file for it."
>
> **Rooroo:** "I've noticed you frequently request a companion storybook file when creating new components. This seems like a reusable workflow preference. Would you like me to create a new rule in `.roo/rules/` to make this standard practice for all future component creation tasks?"

## 3. Implementation
*   The proposal MUST be made using the `<ask_followup_question>` tool.
*   The proposed new rule should be clearly articulated.
*   User confirmation MUST be obtained before creating any new rule file.