# MCP Autonomous Traders

MCP Autonomous Traders is a modular Python framework for building, running, and experimenting with autonomous trading agents. It supports research, trading, and portfolio management workflows, and is designed for extensibility and integration with multiple data sources and agent models.

## Features
- Modular agent and tool architecture
- Integration with multiple LLM providers (OpenAI, DeepSeek, Grok, Gemini, OpenRouter)
- Researcher and trader agent roles
- Persistent memory and knowledge graph support
- Automated trading and rebalancing workflows
- Environment variable configuration for API keys

## Requirements
- Python 3.12+
- [uv](https://github.com/astral-sh/uv) (for dependency management and running)

## Installation
1. **Clone the repository:**
   ```sh
   git clone <your-repo-url>
   cd mcp-autonomous-traders
   ```
2. **Install dependencies using uv:**
   ```sh
   uv pip install -r requirements.txt  # If requirements.txt exists
   # or, to add dependencies:
   uv add openai python-dotenv
   ```
   > **Note:** If you use additional agent, tracer, or account client packages, add them as needed:
   > ```sh
   > uv add <package-name>
   > ```

## Configuration
Set the following environment variables in a `.env` file or your shell:
- `OPENAI_API_KEY` (for OpenAI models)
- `DEEPSEEK_API_KEY` (for DeepSeek models)
- `GROK_API_KEY` (for Grok models)
- `GOOGLE_API_KEY` (for Gemini models)
- `OPENROUTER_API_KEY` (for OpenRouter models)
- `BRAVE_API_KEY` (for Brave search)
- `POLYGON_API_KEY` (for Polygon market data)

Example `.env`:
```
OPENAI_API_KEY=your-openai-key
DEEPSEEK_API_KEY=your-deepseek-key
GROK_API_KEY=your-grok-key
GOOGLE_API_KEY=your-google-key
OPENROUTER_API_KEY=your-openrouter-key
BRAVE_API_KEY=your-brave-key
POLYGON_API_KEY=your-polygon-key
```

## Usage
Run the main entry point:
```sh
uv run main.py
```

## Project Structure
- `main.py` — Entry point
- `traders.py` — Trader agent logic
- `templates.py` — Prompt and message templates
- `mcp_params.py` — MCP server configuration
