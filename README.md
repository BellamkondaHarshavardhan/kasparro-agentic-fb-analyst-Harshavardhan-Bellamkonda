# kasparro-agentic-fb-analyst-Harshavardhan-Bellamkonda

An agentic LLM pipeline that autonomously analyzes Facebook Ads performance, diagnoses ROAS drops, validates every insight against real data, and generates fresh creative recommendations.

## Overview
- Analyzed the provided synthetic undergarments Facebook Ads dataset
- Built a Planner → Evaluator → Generator architecture with quantitative validation
- Zero hallucinated numbers (Evaluator loop checks every metric against the CSV)

## Setup (if someone wants to run it)
```bash
pip install pandas langchain openai python-dotenv
