# mcp-demo
<img width="1416" height="814" alt="Screen Shot 2025-09-01 at 8 19 36 PM" src="https://github.com/user-attachments/assets/cf5f3a76-a3ce-41e9-b264-78c5ffc7ad49" />

# MCP Demo — Client + Gemini API

## Overview

This repository contains a single-page, client-side demonstration of a **Model Context Protocol (MCP)** system designed for portfolio and technical showcase purposes. The implementation is fully static and runs entirely in the browser using JavaScript, with optional integration for Google Gemini API. No server-side components are required.

The MCP system illustrates key principles of agentic reasoning workflows:

- **Observe:** Accepts user input and context documents.
- **Think:** Applies model-specific logic or calls the Gemini API.
- **Act:** Produces structured outputs, reasoning traces, or mock summaries.

## Features

1. **Client-only MCP Simulation**
   - Multiple mock models including `echo-v0`, `assistant-sim`, and `cot-sim`.
   - Supports context ingestion, addition, removal, and clearing.
   - Temperature slider for simulating stochastic output.

2. **Gemini API Integration**
   - Users can supply their own Gemini API key.
   - Performs real-time requests to Gemini for model output.
   - Fully encapsulated in client-side JavaScript.

3. **Interactive Chat Interface**
   - Chat messages with timestamps.
   - User vs model differentiation.
   - Simulated reasoning chain execution with step-by-step traces.

4. **Portfolio-ready**
   - Fully static HTML page (`index.html`).
   - Mobile-responsive layout with custom CSS.
   - Modern aesthetic using gradient backgrounds, soft shadows, and typography via Google Fonts.

## File Structure

### Interacting with MCP

- **Models:** Select a model from the sidebar (`Echo`, `Assistant Sim`, `Chain-of-Thought Sim`, `Gemini API`).
- **Context:** Add text snippets or system prompts to the context panel. Contexts can be removed or cleared.
- **Temperature:** Adjust the slider to influence stochastic output (mock behavior).
- **User Input:** Enter prompts in the textarea and press `Send`.
- **Chain Simulation:** Press `Run Reasoning Chain` to observe stepwise reasoning simulation.

### Gemini API Integration

- Enter a valid Gemini API key in the designated input field.
- Switch the active model to `Gemini API (live)`.
- All subsequent prompts will be sent to the Gemini model, returning live responses.

## Technical Details

### Mock Models

- **Echo Model (`echo-v0`)**: Returns the user input verbatim. Minimal processing; demonstrates simple output mapping.
- **Assistant Sim (`assistant-sim`)**: Provides simulated summarization or extraction from context. Uses basic string operations to truncate or bullet content.
- **Chain-of-Thought Sim (`cot-sim`)**: Demonstrates stepwise reasoning: `Observe -> Think -> Act`. Returns both reasoning trace and a conclusion placeholder.
