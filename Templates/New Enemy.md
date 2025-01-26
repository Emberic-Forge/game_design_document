---
faction: <% await tp.system.suggester((item) => item, ["Bandit", "Holy Monarch Unit", "Rogue", "Void Occult", "Natural", "Corrupt" ]) %>
category:  <% await tp.system.suggester((item) => item, ["Normal", "Mini-Boss", "Boss" ]) %>
---
<%* 
let title = await tp.system.prompt("Write a name")
await tp.file.rename(title) 
%>
# <%* tR += `${title}` %>

> [!summary] Description
> <% await tp.system.prompt("Describe the enemy", null, false, true) %>

---

>[!warning] Behaviour
<%*
let prompt = await tp.system.prompt("Describe its behaviour", null, false, true);
let result = ""
prompt.split(`\n`).forEach(line => {
	result += `> ${line}\n`
});
tR += result;
%>

>[!warning] Ability
<%*
prompt = await tp.system.prompt("Describe its abilities", null, false, true);
result = ""
prompt.split(`\n`).forEach(line => {
	result += `> ${line}\n`
});
tR += result;
%>
