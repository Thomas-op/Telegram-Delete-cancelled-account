from pyrogram import filters, Client
from time import sleep

app = Client("qwerty", api_id=Your api_ id, api_hash="Your api_hash", phone_number="+Your phone")

banner = """
   [ Send in group : delete ]
"""

print(banner)
counter = 1
@app.on_message(filters.me & filters.text)
def main(c, m):
    global counter
    if m.text == "delete":
        for i in app.get_chat_members(m.chat.id):
            if i.user.is_deleted:
                ids = i.user.id
                app.ban_chat_member(m.chat.id, ids)
                print("Kicked "+str(counter))
                sleep(3)
                counter += 1
app.run()
