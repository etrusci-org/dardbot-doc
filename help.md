# Data the Discord Bot - Help




## Commands

Prefix for all commands is `?`.  
Some commands work only for special users.  
Both commands and arguments are case-insensitive.  
Multiple arguments are separated with commas.  
Invalid user input will be silently ignored in most cases.  
`<argument>`=required `[argument]`=optional `|`=or

| Command  | Alias   | Arguments                                       | Permission |
|----------|---------|-------------------------------------------------|------------|
| `animal` | `a`     | `[cat \| dog]`                                  | users      |
| `enigma` | `e`     |                                                 | users      |
| `help`   | `h`     |                                                 | users      |
| `leet`   | `eleet` | `<any_text>`                                    | users      |
| `music`  | `m`     | `[search_query [, artist \| label \| release]]` | users      |
| `quote`  | `q`     |                                                 | users      |
| `sys`    |         |                                                 | admins     |
| `time`   | `t`     | `<zone1> [[, zone2][, zone3][, zone10]]`        | users      |


### Command: animal

Display random cat and dog pictures.

**Alias**: `a`  
**Arguments**: `[cat | dog]`

When called without argument, a random choice will be made between `cat` and `dog`.

**Usage**:
```text
?animal
?animal cat
?animal dog
?a
?a cat
?a dog
```


### Command: enigma

Display a random enigmatic phrase (and probably learn a lot of new english words in the process).

**Alias**: `e`  
**Arguments**: *none*

**Usage**:
```text
?enigma
?e
```


### Command: help

Display the link to the user guide.

**Alias**: `h`  
**Arguments**: *none*

**Usage**:
```text
?help
?h
```


### Command: leet

Translate text into leetspeak.

**Alias**: `eleet`  
**Arguments**: `<any_text>`

When called with the alias `eleet`, the translation will be more complex.

**Usage**:
```text
?leet The quick brown fox, jumps over the lazy dog.
?eleet The quick brown fox, jumps over the lazy dog.
```


### Command: music

Query the Discogs database.

**Alias**: `m`  
**Arguments**: `[search_query [, artist | label | release]]`

When called without arguments, a random release will be returned.
When only `search_query` is provided, the search will be made across artist, label and release.
When the second argument is provided, the search will be limited to this type.

**Usage**:
```text
?music
?music wu-tang clan 36 chambers
?music wu-tang clan, artist
?music n5md, label
?music kopfnicker, release
?m
?m wu-tang clan 36 chambers
?m wu-tang clan, artist
?m n5md, label
?m kopfnicker, release
```


### Command: quote

Display a random quote.

**Alias**: `q`  
**Arguments**: *none*

**Usage**:
```text
?quote
?q
```


### Command: sys

Display system information.

**Alias**: *none*  
**Arguments**: *none*

**Usage**:
```text
?sys
```


### Command: time

Display the current time of one or more timezones.

**Alias**: `t`  
**Arguments**: `<zone1> [[, zone2][, zone3][, zone10]]`

Zone queries are case-insensitive and can be partial. E.g. `os an` will match `Los Angeles`.

```text
?time tokyo
?time tokyo, sydney, zurich, los angeles
?time toky, sydn, zuri, os an
?t tokyo
?t tokyo, sydney, zurich, los angeles
?t toky, sydn, zuri, os an
```
