## Add this to your agent configs:
```
"mcpServers": {
  "discord": {
    "command": "docker",
    "args": ["run", "--rm", "-i",
        "-e", "DISCORD_TOKEN=<...>",
        "-e", "DISCORD_GUILD_ID=<...>",
        "saseq/discord-mcp:latest"]
  }
}
```

