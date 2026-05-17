<%*
const problemNum = await tp.system.prompt("Номер задачи (например: 15)")
const problemTitle = await tp.system.prompt("Название задачи (например: 3Sum)")
const title = `LeetCode ${problemNum} – ${problemTitle}`
const filename = tp.date.now("YYYYMMDDHHmm") + " – " + title;
await tp.file.rename(filename);
%>---
id: <% tp.date.now("YYYYMMDDHHmmss") %>
type: zettel
tags: [leetcode]
aliases: ["<% `LC${problemNum}` %>"]
source: https://leetcode.com/problems/<% problemTitle.toLowerCase().replace(/\s+/g, '-').replace(/[^a-z0-9-]/g, '') %>/
difficulty: Medium
topic: []
status: in-progress
created: <% tp.date.now("YYYY-MM-DD") %>
updated: <% tp.date.now("YYYY-MM-DD") %>
---
# LeetCode <% problemNum %> – <% problemTitle %>

## Задача

> Своими словами — что нужно сделать? Какой вход, какой выход?



## Первая реакция

> До решения: что приходит в голову? Какие структуры данных/алгоритмы?



## Подходы

### ❌ Подход 1 — (название)

**Идея:**

**Почему не работает / слишком медленно:**

---

### ✅ Финальный подход — (название)

**Ключевой инсайт (одна фраза):**

**Алгоритм по шагам:**
1. 
2. 
3. 

**Код (ключевые фрагменты):**
```

```

**Сложность:**
- Время: O( )
- Память: O( )

## Что было сложно

> Где застрял? Что не очевидно? Что пришлось гуглить?



## Вопросы и TODO

- [ ] 

## Связана с

- [[MOC — LeetCode]]
- 
