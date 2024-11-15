---
layout: default
---

## Commands Overview

The more you know...
- Prefix for all commands is `{{ site.data.shared.command_prefix }}`.
- Both commands and arguments are case-insensitive.
- Multiple arguments are separated with commas.
- Invalid user input will be silently ignored in most cases.
- `<argument>`=required `[argument]`=optional `|`=or

For examples click a command below.

| Command | Alias | Arguments | Permission |
|---------|-------|-----------|------------|
{% for cmd in site.data.commands %}| [{{ cmd[0] }}](./command-{{ cmd[0] }}.html) | {% if cmd[1].alias %}`{{ cmd[1].alias }}`{% else %}*none*{% endif %} | {% if cmd[1].arguments %}`{{ cmd[1].arguments }}`{% else %}*none*{% endif %} | {{ cmd[1].permission }} |
{% endfor %}
