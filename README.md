# AI Investment Agent (סוכן השקעות חכם)

This repository contains the logic and prompts for an AI Investment Agent designed to operate within an Obsidian Vault environment using Claude Code.

## Overview
The Investment Agent manages, analyzes, and provides insights on your investment portfolio. It is broken down into specific skills that a central AI agent can lazy-load when analyzing the market or user's portfolio.

## Files included:
- `SKILL-investment-agent.md`: The core identity and tasks of the investment agent.
- `SKILL-investment-research.md`: The skill containing rules and heuristics for deep market research.
- `SKILL-investment-swing.md`: The skill dedicated to analyzing short-term swing trading opportunities.
- `Portfolio.md`: The portfolio file which contains all the data relevant to you/

## Usage
To use these skills with an AI agent (e.g., Claude Code), place these files in your system prompts/skills directory, and let the agent load them dynamically when queried about investments, stock market, or portfolio management.
