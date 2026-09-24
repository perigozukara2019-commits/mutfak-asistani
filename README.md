# Kitchen Assistant 🍳

A simple AI assistant that suggests healthy recipes for two people, using only the ingredients I have at home.

This is my first AI assistant project, built as part of my learning roadmap. It uses no code: just clear instructions and well-structured context files, set up as a Claude Project.

## How it works
An AI assistant is built from three parts:

1. **Task** – what the assistant does
2. **Context** – what the assistant needs to know
3. **Boundaries** – what the assistant must never do

| File | Purpose |
|---|---|
| `talimat.md` | Instructions: the task, response format and boundaries |
| `mutfak-bilgileri.md` | Context: our tastes, kitchen tools, time and pantry staples |
| `saglik.md` | Private dietary notes – **not in this repo** (excluded with `.gitignore`) |

## Usage
I write the ingredients I have today. The assistant suggests up to 3 recipes, each with time, ingredients, steps and a short note on why it is healthy.

## Privacy
Health information is sensitive. It stays in a separate file on my computer and is excluded from GitHub with `.gitignore`. I tested this with `git status` before the first commit.

## Testing and improving
I tested the assistant with real ingredients and checked each answer against its rules.

- **First test:** The assistant *assumed* basic items like salt and olive oil were at home, and skipped lemon because it was not listed.
- **Change:** I added a "pantry staples" list to the context and made the instructions clearer ("only" instead of "first").
- **Second test:** With the same ingredients, it used lemon and spices without guessing, and listed missing ingredients for every recipe.

Same question, different context, better answer.

## What I learned
- Vague words (like "healthy") must be turned into clear, checkable rules.
- Conflicting information confuses the assistant and must be resolved with one clear rule.
- Always write down the source of important information.
- When one file changes, check the files connected to it.
- Evaluate answers against the original question, not just whether they look good.

## Disclaimer
This assistant does not give medical advice. Doctor's recommendations always come first.