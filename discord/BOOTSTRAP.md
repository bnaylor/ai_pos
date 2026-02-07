# Discord Bootstrap & Identity Mapping

This file persists the mapping of bot identities and the human owner on Discord.

## 👤 Human Owner
- **Username:** [e.g., scromp]
- **User ID:** [To be filled by agent on first discovery]

## 🤖 Agent Identities
- **Gemini Bot ID:** [To be filled by Gemini]
- **Claude Bot ID:** [To be filled by Claude]

## 🏠 Primary Channel
- **Server (Guild) ID:** [From MCP Config]
- **Coordination Channel ID:** [To be filled by agent]

## 🛠 Bootstrap Process
1.  **Detection:** Upon first launch with Discord MCP, the agent should search for the coordination channel and the human owner.
2.  **Mapping:** Post a message asking the other agent for its ID (if not already known).
3.  **Persistence:** Write the discovered IDs to this file to avoid re-discovery in future sessions.
