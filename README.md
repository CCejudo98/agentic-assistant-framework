# Agentic Assistant Framework

A cybernetic and systems-theory framework for designing, versioning, and deploying domain-specific virtual assistant architectures using **Google AI Studio**, **Gemini API**, and advanced system prompt engineering.

---

## Overview

This repository treats system instructions as production code (**Prompt-as-Code**). It provides structured modules for state management, variety reduction (Ashby's Law), transductive workflow regulation, and structured output formatting across multi-turn LLM interactions.

```text
agentic-assistant-framework/
├── config/
│   ├── system_prompt_charm.md    # Human regulation, biomechanics & associated medium
│   ├── system_prompt_ideal.md    # IDEAL transducer & meta-prompt compiler
│   └── system_prompt_audit.md    # Socio-technical & governance auditor
├── workflows/
│   ├── calendar_kernel.md        # Execution flow & calendar sync protocol
│   └── variety_attenuators.md    # Friction reduction & systemic guardrails
└── README.md                     # Core framework documentation
import google.generativeai as genai

genai.configure(api_key="YOUR_API_KEY")

with open("config/system_prompt_charm.md", "r") as f:
    system_instruction = f.read()

model = genai.GenerativeModel(
    model_name="gemini-1.5-pro",
    system_instruction=system_instruction
)

chat = model.start_chat(history=[])
response = chat.send_message("Initialize operational state.")
print(response.text)
