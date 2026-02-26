# polymrkt

**AI-powered Polymarket trading simulator.** polymrkt connects to live Polymarket prediction markets, runs Mistral AI analysis via Ollama to surface trade recommendations with entry side, stake, stop-loss, and take-profit levels, then tracks your simulated portfolio in real time. It is a full stack Node.js app with a clean browser UI — no exchange account or real money required.

> 📸 *screenshot*

---

**Features**

- Live market data pulled from the Polymarket Gamma API — sorted by 24h volume, filtered by category
- Mistral AI analysis (via Ollama) with up to 3 ranked recommendations per run, each with reasoning
- Auto mode — runs analysis on a loop and executes the top recommendation automatically
- Manual mode — review AI picks before committing
- Stop-loss, take-profit, and trailing-stop on every position
- Portfolio dashboard with real-time P&L, win rate, and trade history
- Category tabs (Sports · Politics · Finance · Crypto · Trending) with live sparklines and activity indicators
- MCP server — expose polymrkt as native tools inside Claude Desktop, Cursor, or Windsurf; ask questions in plain English and get live portfolio data back
- OpenAPI 3.0 spec at `/api/openapi.yaml` for LangChain, AutoGen, and any HTTP agent framework
- KVM accessible — runs headlessly on a remote machine; point the MCP server at it with `POLYMRKT_URL` and control it from any Claude client on your network
