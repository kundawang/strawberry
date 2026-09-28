---
release type: patch
social_messages:
  x: >-
    {project_name} {version} is out! This release fixes a crash in the legacy
    graphql-ws protocol when receiving malformed JSON messages. 🍓
    https://strawberry.rocks/release/{version}
  linkedin: >-
    {project_name} {version} is out. This release fixes a crash in the legacy
    graphql-ws WebSocket protocol handler when receiving JSON messages that are
    not valid operation messages, such as `null`, numbers, or objects without a
    "type" key. These messages are now ignored instead of crashing the
    connection.
---

This release fixes a crash in the legacy `graphql-ws` WebSocket protocol
handler when receiving JSON messages that are not valid operation messages.

Messages like `null`, numbers, strings, lists, or objects without a `"type"`
key are now ignored at every stage of the protocol, instead of crashing the
connection handler. This applies to all framework integrations (aiohttp, ASGI,
Channels, FastAPI, Litestar and Quart).
