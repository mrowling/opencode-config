# Opencode Config

This repository contains my personal opencode configuration.

## Ralph

It includes custom skills and the Ralph script based on https://github.com/snarktank/ralph

### Workflow

#### 1. Create a PRD

Use the PRD skill to generate a detailed requirements document:

```
Create a PRD for [your feature description]
```

Answer the clarifying questions. The skill saves output to `tasks/prd-[feature-name].md`.

#### 2. Convert PRD to Ralph format

Use the Ralph skill to convert the markdown PRD to JSON:

```
Load the ralph skill and convert tasks/prd-[feature-name].md to prd.json
```

This creates `prd.json` with user stories structured for autonomous execution.

#### 3. Run Ralph

```bash
ralph [max_iterations]
```