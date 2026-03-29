<%* 
const title = (await tp.system.prompt("Title"))
const filename = tp.date.now("YYYYMMDDHHmm") + " – " + title;
await tp.file.rename(filename);
%>---
id: <% tp.date.now("YYYYMMDDHHmmss") %>
type: literature
tags: [литература]
aliases: []
source: ""
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
---
# <% title %>

## Основные идеи


## Цитаты


## Мои мысли


## Связана с
