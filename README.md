<div align="center">
  <img src="https://play-lh.googleusercontent.com/WDoP-Jos3M3Y7Kp5ihcOdYFhf50u_flPHvx2j0YjFh-0cv8aQZo11eDkNo7qFTZWyq29" height="60">
  <h1>capture.py</h1>

> Mobile-API for [capture](https://play.google.com/store/apps/details?id=com.capture.tech) social network </div>

---

## Usage

```python
from capture import Capture

client = Capture()
client.login_with_x_token("your_x_token")

# Send a message
client.send_message(chat_id=123, text="Hello!")

# Search for chats
results = client.search_chats("gaming")
print(results)

# Edit your profile
client.edit_profile(name="John", bio="Hello world", location="NYC")
```

---

## Methods

### Auth

| Method | Description |
|--------|-------------|
| `login_with_google(google_id_token)` | Log in using a Google ID token |
| `login_with_x_token(x_token)` | Log in using an X-Token and set session |
| `register(username)` | Register a new account with a username |
| `register_with_google(google_id_token, username)` | Register using a Google ID token and username |

---

### Account

| Method | Description |
|--------|-------------|
| `get_account_info()` | Get current account info |
| `edit_profile(name, bio, location, status)` | Edit profile details |
| `get_notifications()` | Get account notifications |
| `get_config()` | Get app config |
| `get_ml_config()` | Get ML config |
| `get_stickers()` | Get available stickers |
| `get_trending_gifs()` | Get trending GIFs |
| `search_gifs(query)` | Search for GIFs |
| `get_link_preview(url)` | Get a preview for a URL |

---

### Users

| Method | Description |
|--------|-------------|
| `get_user(user_id)` | Get a user by ID |
| `get_user_by_username(username)` | Get a user by username |
| `get_user_badges(user_id)` | Get a user's badges |
| `get_user_chats(user_id, count)` | Get chats a user is in |
| `send_direct_message_request(user_id)` | Send a DM request to a user |
| `get_direct_messages_requests()` | Get pending DM requests |
| `report_user(user_id, reason, comment)` | Report a user |

---

### Chats

| Method | Description |
|--------|-------------|
| `get_chats(count)` | Get joined chats |
| `get_all_chats()` | Get all chats |
| `get_chat(chat_id)` | Get a chat by ID |
| `get_chat_by_link(link)` | Get a chat by invite link |
| `create_chat(content, name, is_channel, is_private)` | Create a new chat |
| `edit_chat(chat_id, description, name, category_id)` | Edit a chat |
| `join_chat(chat_id)` | Join a chat |
| `leave_chat(chat_id)` | Leave a chat |
| `follow_chat(chat_id)` | Follow a chat |
| `unfollow_chat(chat_id)` | Unfollow a chat |
| `search_chats(query)` | Search for chats |
| `unread(chat_id)` | Mark a chat as unread |
| `update_chat_settings(chat_id, sound, mute)` | Update chat notification settings |
| `get_discover_items(count)` | Get discover feed items |
| `get_discover_onboarding()` | Get onboarding discover content |
| `report_chat(chat_id, reason, comment)` | Report a chat |

---

### Chat Members

| Method | Description |
|--------|-------------|
| `get_chat_users(chat_id, count)` | Get members of a chat |
| `set_chat_user_role(chat_id, user_id, role)` | Set a member's role |
| `ban(chat_id, user_id)` | Ban a user from a chat |
| `unban(chat_id, user_id)` | Unban a user from a chat |
| `search_mention_users(chat_id, prefix)` | Search mentionable users in a chat |

---

### Messages

| Method | Description |
|--------|-------------|
| `get_chat_messages(chat_id, count)` | Get messages from a chat |
| `send_message(chat_id, text, quote_message_id, gif_id, gif_provider)` | Send a message |
| `edit_message(chat_id, message_id, text)` | Edit a message |
| `delete_message(chat_id, message_id)` | Delete a message |
| `post_typing(chat_id, status)` | Post a typing indicator |
| `report_message(chat_id, message_id, reason, comment)` | Report a message |

---

### Photos

| Method | Description |
|--------|-------------|
| `get_chat_photos(chat_id, count, reverse)` | Get photos from a chat |
| `get_relevant_chat_photos(chat_id, count)` | Get ML-ranked relevant photos |

---

### Communities

| Method | Description |
|--------|-------------|
| `get_joined_communities()` | Get joined communities |
| `get_discover_communities()` | Discover public communities |
| `get_community(com_id)` | Get a community by ID |
| `get_community_chats(com_id)` | Get chats in a community |
| `follow_community(com_id)` | Join a community |
| `unfollow_community(com_id)` | Leave a community |
| `remove_chat_from_community(com_id, chat_id)` | Remove a chat from a community |

---

---

> **Note:** Also note there is a typo in `__init__` - `session_id: str = None))` has an extra closing parenthesis that should be removed.
