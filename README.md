# 🔥 MRSILENT Programming Language v2.0

**A Complete, Telegram-Bot-Ready Scripting Language**

![Version](https://img.shields.io/badge/version-2.0.0-blue)
![Language](https://img.shields.io/badge/language-MRSILENT-red)
![Status](https://img.shields.io/badge/status-Production%20Ready-green)

---

## 📋 Table of Contents

1. [Overview](#overview)
2. [Core Language Syntax](#core-language-syntax)
3. [Built-in Modules](#built-in-modules)
4. [Bot Module Reference (40+ Functions)](#bot-module-reference)
5. [User Data Module](#user-data-module)
6. [Database Module](#database-module)
7. [HTTP Module](#http-module)
8. [AI Module](#ai-module)
9. [Utility Module](#utility-module)
10. [Globals Reference](#globals-reference)
11. [Full Bot Example](#full-bot-example)
12. [Security Model](#security-model)

---

## 🎯 Overview

**MRSILENT** is an ultra-compact scripting language that compiles to
Python. Version 2.0 adds a complete set of built-in modules so you
can write fully working Telegram bots, AI integrations, and HTTP-
connected tools - without leaving MRSILENT syntax.

- **Created by**: MR.SILENT (@xenovoidx)
- **Version**: 2.0.0
- **Compiles to**: Python (runs via a safe execution sandbox)
- **Built-in modules**: `bot`, `user`, `db`, `http`, `ai`, `util`
- **Total built-in functions**: 40+

---

## 💻 Core Language Syntax

(Unchanged from v1 - still applies on top of everything below.)

```
x = 10, name = "Sumit"              # variables
add = (a, b) => a + b               # arrow function
fn calc(a, b) { return a + b }      # named function
x > 5 ? "Big" : "Small"             # ternary
if x > 5 { } else { }               # if-else
loop(i, 0, 10) { }                  # for loop
while x > 0 { }                     # while loop
[1, 2, 3, 4]                        # array
"Hello {name}"                      # string interpolation
```

---

## 📦 Built-in Modules

Import any module at the top of your file:

```
import "bot" as bot
import "user" as user
import "db" as db
import "http" as http
import "ai" as ai
import "util" as util
```

All modules are available automatically once imported - no install
step needed, they're built into the MRSILENT runtime.

---

## 🤖 Bot Module Reference

`import "bot" as bot` gives you full control over your Telegram bot.

### Messaging

| Function | Arguments | Description |
|---|---|---|
| `bot.message(text)` | text | Sends a text message to the current chat |
| `bot.reply(text)` | text | Replies to the current incoming message |
| `bot.send(chat_id, text)` | chat_id, text | Sends a message to any specific chat/user |
| `bot.edit(message_id, text)` | message_id, text | Edits an existing message's text |
| `bot.delete(message_id)` | message_id | Deletes a message |
| `bot.pin(message_id)` | message_id | Pins a message in the chat |
| `bot.unpin(message_id)` | message_id | Unpins a message |

### Media

| Function | Arguments | Description |
|---|---|---|
| `bot.photo(url, caption)` | url, caption | Sends a photo |
| `bot.video(url, caption)` | url, caption | Sends a video |
| `bot.audio(url, caption)` | url, caption | Sends an audio file |
| `bot.document(url, caption)` | url, caption | Sends a document/file |
| `bot.sticker(file_id)` | file_id | Sends a sticker |
| `bot.animation(url, caption)` | url, caption | Sends a GIF/animation |
| `bot.voice(url)` | url | Sends a voice note |

### Group / Member Management

| Function | Arguments | Description |
|---|---|---|
| `bot.ban(user_id)` | user_id | Bans a user from the group |
| `bot.unban(user_id)` | user_id | Unbans a user |
| `bot.mute(user_id, seconds)` | user_id, seconds | Restricts a user from sending messages |
| `bot.unmute(user_id)` | user_id | Removes restrictions on a user |
| `bot.promote(user_id)` | user_id | Promotes a user to admin |
| `bot.demote(user_id)` | user_id | Removes admin rights |
| `bot.kick(user_id)` | user_id | Kicks a user (ban + immediate unban) |
| `bot.setTitle(title)` | title | Changes the group's title |
| `bot.memberCount()` | none | Returns the chat's member count |
| `bot.chatInfo()` | none | Returns info about the current chat |
| `bot.isAdmin(user_id)` | user_id | Checks if a user is a group admin |

### Buttons & Keyboards

| Function | Arguments | Description |
|---|---|---|
| `bot.button(text, data)` | text, data | Creates one inline button |
| `bot.keyboard(rows)` | rows (array of button arrays) | Creates an inline keyboard layout |
| `bot.replyKeyboard(rows)` | rows | Creates a reply (non-inline) keyboard |
| `bot.removeKeyboard()` | none | Removes any active keyboard |
| `bot.answerCallback(text)` | text | Answers a button press (callback query) |

### Scheduling & Flow

| Function | Arguments | Description |
|---|---|---|
| `bot.after(seconds, command)` | seconds, command name | Runs a command after a delay |
| `bot.run(command)` | command name | Immediately runs another command |
| `bot.broadcast(text)` | text | Sends a message to every known user |
| `bot.typing()` | none | Shows the "typing..." indicator |

### Bot Info

| Function | Arguments | Description |
|---|---|---|
| `bot.info()` | none | Returns the bot's own profile info |
| `bot.setName(name)` | name | Sets the bot's display name |
| `bot.setDescription(text)` | text | Sets the bot's description |

That's **34 bot functions** - combined with the modules below, you
get well past 40 built-ins total.

---

## 👤 User Data Module

`import "user" as user`

| Function | Arguments | Description |
|---|---|---|
| `user.save(key, value)` | key, value | Saves a value for the current user |
| `user.get(key)` | key | Retrieves a value for the current user |
| `user.delete(key)` | key | Deletes a saved value |
| `user.exists(key)` | key | Checks if a key exists for this user |
| `user.all()` | none | Returns all saved data for this user |

---

## 🗄️ Database Module

`import "db" as db`

| Function | Arguments | Description |
|---|---|---|
| `db.save(key, value)` | key, value | Saves a global (bot-wide) value |
| `db.get(key)` | key | Retrieves a global value |
| `db.delete(key)` | key | Deletes a global value |
| `db.exists(key)` | key | Checks if a global key exists |
| `db.count()` | none | Returns the number of saved keys |

---

## 🌐 HTTP Module

`import "http" as http`

| Function | Arguments | Description |
|---|---|---|
| `http.get(url)` | url | Sends a GET request, returns response object |
| `http.post(url, data)` | url, data | Sends a POST request with JSON data |
| `http.put(url, data)` | url, data | Sends a PUT request |
| `http.delete(url)` | url | Sends a DELETE request |

Response object methods: `.json()`, `.text()`, `.status()`

---

## 🧠 AI Module

`import "ai" as ai`

| Function | Arguments | Description |
|---|---|---|
| `ai.ask(prompt)` | prompt | Sends a prompt to the configured AI model, returns the reply |
| `ai.chat(prompt, history)` | prompt, history array | Same as `ask`, but with conversation memory |

---

## 🛠️ Utility Module

`import "util" as util`

| Function | Arguments | Description |
|---|---|---|
| `util.random(min, max)` | min, max | Random integer in range |
| `util.randomStr(length)` | length | Random alphanumeric string |
| `util.now()` | none | Current timestamp |
| `util.uuid()` | none | Generates a unique ID |

---

## 🌍 Globals Reference

These variables are automatically available in every command,
no import needed:

| Global | Description |
|---|---|
| `text` | The raw text of the incoming message |
| `user_id` | The ID of the user who sent the message |
| `chat_id` | The ID of the current chat (group or private) |
| `username` | The username of the sender (may be empty) |
| `first_name` | The sender's first name |
| `is_group` | `true` if the message is from a group/supergroup |
| `command_args` | Any text after the command, e.g. `/ban 123 spam` → `"123 spam"` |

---

## 💡 Full Bot Example

```
import "bot" as bot
import "user" as user
import "ai" as ai

fn start_command() {
    bot.reply("Hii {first_name}! Main MRSILENT se bana bot hu 🔥")
}

fn balance_command() {
    bal = user.get("balance") ?? 0
    bot.reply("Your balance: {bal}")
}

fn chat_command() {
    reply = ai.ask(text)
    bot.reply(reply)
}

fn ban_command() {
    is_group && bot.isAdmin(user_id) ? bot.ban(user_id) : bot.reply("Admins only!")
}
```

---

## 🔒 Security Model

MRSILENT programs run inside a restricted execution sandbox:

- No direct file system access
- No `import` of arbitrary Python modules - only the 6 built-in
  MRSILENT modules above are available
- No `eval`/`exec` exposed to user code
- Network access only through the `http` module (which can be
  rate-limited/monitored)
- Each bot's data (`user.*`, `db.*`) is isolated from other bots

This mirrors how production bot platforms keep user-submitted code
safe while still being genuinely powerful.

---

## 📞 Support

- **Developer**: MR.SILENT (@xenovoidx)
- **License**: MIT - Free to use

```
Write less. Do more. 🔥
```
