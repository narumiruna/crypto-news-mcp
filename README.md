# Crypto News MCP Server

## TODO

- [x] coindesk
- [x] [decrypt](https://decrypt.co/)

## Usage

From PyPI

```json
{
  "mcpServers": {
    "cryptonewsmcp": {
      "command": "uvx",
      "args": ["cryptonewsmcp"]
    }
  }
}
```

From GitHub

```json
{
  "mcpServers": {
    "cryptonewsmcp": {
      "command": "uvx",
      "args": [
        "--from",
        "git+https://github.com/narumiruna/crypto-news-mcp",
        "cryptonewsmcp"
      ]
    }
  }
}
```

## Components

### Tools

- recent_news
  - Fetches latest crypto news from specified site
  - Input:
    - site: Source site ("coindesk" or "decrypt")
  - Returns formatted list of news entries with titles, links, dates and summaries
- read_news
  - Fetches article HTML from URL and converts it to Markdown
  - Input:
    - url: Article URL to retrieve
  - Returns Markdown-formatted article content
