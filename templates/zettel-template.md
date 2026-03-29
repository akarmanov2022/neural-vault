<%* 
const title = (await tp.system.prompt("Title"))
const filename = tp.date.now("YYYYMMDDHHmm") + " – " + title;
await tp.file.rename(filename);
%>---
id: <% tp.date.now("YYYYMMDDHHmmss") %>
type: zettel
tags: []
aliases: []
source: 
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
---
# <% title %>



## Связана с
