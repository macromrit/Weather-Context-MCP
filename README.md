# 🌦️ Weather MCP Server

This is a minimal FastMCP server that serves as a weather alert provider. It allows MCP clients and LLM agents to query real-time weather alerts for U.S. states using the National Weather Service API.

---

## 📌 Purpose

This server is designed to be used in multimodal cognition pipelines or by MCP clients to:

- 🔎 Fetch live weather alerts per U.S. state.
- 🧠 Expose tool-like interfaces usable by LLMs or agentic systems.
- 🔁 Provide a simple echo resource for diagnostics.

---

## ▶️ How to Run

### 1. Install requirements

```
uv add 'mcp[cli]'
```

### 2. Start the MCP server

```bash
uv run server.py
```

This will start the FastMCP server defined in `server.py`.

---

## 🧠 Exposed Tools

### `get_alerts(state: str) -> str`

Returns formatted weather alerts for the given U.S. state.

Example usage:

```python
get_alerts("NY")
```

---

## 🔁 Resources

### `echo://{message}`

A simple resource that echoes back the message.

---

## 📝 Notes

* This app uses the public [weather.gov](https://www.weather.gov/) API (no authentication required).
* Works well as a plug-in context provider for AI agents or assistant frameworks using MCP.
