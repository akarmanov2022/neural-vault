<%* 
const title = (await tp.system.prompt("Title"))
const filename = tp.date.now("YYYYMMDDHHmm") + " – " + title;
const folder = "01 fleeting notes";
await tp.file.rename(filename);
%>---
id: <% tp.date.now("YYYYMMDDHHmmss") %>
tags: []
aliases: []
---
# <% title %>

## Связана с
