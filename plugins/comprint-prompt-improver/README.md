# comprint-prompt-improver

Catches vague prompts before they waste your time. Researches your codebase, asks smart questions, then executes with full context.

## How It Works

1. You type a prompt
2. A lightweight hook evaluates if it's clear enough
3. **Clear prompt** → passes through instantly, zero overhead
4. **Vague prompt** → researches your codebase, asks 1-6 targeted questions, then executes with your answers

## Examples

**Vague** — gets enriched:
```
"fix the bug"           → researches recent errors, asks which one
"refactor the code"     → explores codebase, asks scope + approach
"add authentication"    → checks stack, asks auth method + scope
```

**Clear** — passes through:
```
"Refactor getUserById in src/api/users.ts to use async/await"
"Fix the null check in auth.py line 145"
```

## Bypass Prefixes

| Prefix | Effect |
|--------|--------|
| `*` | Skip evaluation entirely |
| `/` | Slash commands pass through |
| `#` | Memory/note commands pass through |

## What Gets Asked

Questions are grounded in actual research — not generic. The skill:
- Checks conversation history first
- Explores your codebase (files, patterns, git history)
- Reads local docs and config
- Generates 1-6 multiple-choice questions based on findings

## Credits

Based on [prompt-improver](https://github.com/severity1/prompt-improver) by severity1. MIT License.
