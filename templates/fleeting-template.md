<%*
const filename = tp.date.now("YYYYMMDDHHmm") + " – Fleeting";
await tp.file.rename(filename);
-%>
---
id: <% tp.date.now("YYYYMMDDHHmmss") %>
type: fleeting
tags: [входящие]
created: <% tp.date.now("YYYY-MM-DD") %>
---
# <% tp.date.now("YYYY-MM-DD HH:mm") %>


## Связана с
