# How to use secret chats in Telegram

Use **secret chats** for added privacy. All messages in secret chats are protected with end-to-end encryption and stored only on participants' devices.  
Secret chats are identified by the 🔒 icon in the title and conversation list.


## How secret chats work

- Secret chats are **not synced** with the Telegram cloud.  
- They are available only on the device where they were created and only during the active session.  
- If you log out, the chat will be deleted automatically.

Secret chats are protected by **MTProto 2.0 end-to-end encryption**.  
Messages are encrypted on your device and decrypted only on the recipient’s device.  
Data are **not stored** on Telegram servers — only you and your recipient can see them.

⚠️ **Warning:**  
Secret chats support secure communication **only between two users**.  
Group secret chats are **not supported**.

When messages are received:
- The text and sender’s name are hidden for added security.  
- By default, screenshots and message forwarding are disabled.  
- You can also enable a **self-destruct timer** for messages and media.

Your partner can **cancel** the secret chat — it will become a regular one.


## How to start a secret chat (Android)

1. Choose a recipient from your contact list.  
   > The recipient must be online to start a secret chat.  
2. Open the main chat with your contact and tap their **profile icon**.  
3. Tap the **three dots** in the top-right corner to open the menu.  
4. Select **Start a Secret Chat**.  
5. In the confirmation window, tap **Start**.  
6. The new secret chat (🔒 icon) will appear in the chat list, and the user’s name will be displayed in **green**.  

You can create multiple secret chats with the same contact.


## How to verify the security of a secret chat (Android)

1. Open the secret chat with your contact.  
2. Tap the contact’s name at the top to open their profile.  
3. Select **Encryption Key**.  
4. You will see an image and text — this is a unique **security key**.  
5. Ask your contact to check if the same image appears on their device.  
6. If the images match, the connection is secure.

⚠️ **Warning:**  
Always verify the key with your contact through a **secure channel** (for example, in person or via an encrypted call).


## How to set a self-destruct timer (Android)

The self-destruct timer automatically deletes a message or media file after the recipient views it.  
Only messages sent *after* enabling the timer will self-destruct.

1. Tap the **three dots** in the top-right corner and select the **clock icon**.  
2. In the *Self-Destruct Timer* window, choose the desired time interval (e.g., 30 seconds).  
3. The timer starts once the recipient opens the message (two check marks appear).  
4. After the timer expires, the message will be deleted from both devices.


## How to delete a secret chat (Android)

1. Tap the **three dots** in the top-right corner and select the **trash bin icon**.  
2. In the confirmation window, check the box to **delete the chat for your contact** (optional).  
3. Tap **Delete**.  
4. The chat will be deleted within 5 seconds.  
   A small countdown panel will appear at the bottom — you can undo the deletion before time runs out.


## Secret chats in Telegram Desktop (fictional feature)

In the desktop version of Telegram, secret chats can include an **optional password or access key** for added protection.  
This example illustrates how it might work.

### Creating a secret chat (Desktop)

1. Open **Telegram Desktop** and go to your contact list.  
2. Select the contact you want to chat with and open their **profile**.  
3. Click the **three-dot icon** and choose **Create Secret Chat**.  
4. When prompted, set a **password** or **key** to protect access.

#### Option 1 — Set a password
1. In the prompt window, click **Create Password**.  
2. Enter a password (minimum 8 characters, unique and secure).  
3. Confirm by re-entering it.  
4. The system will request this password every time you access the chat.

> Passwords are not stored — if you forget it, recovery may not be possible.

#### Option 2 — Create an access key
1. Click **Create Key**.  
2. Telegram will generate a random cryptographic key.  
3. Save it in a secure place — without it, access will be impossible.


### Opening a secret chat (Desktop)

When you try to open the chat, Telegram will ask for the **password or key**.  
Without the correct one, access will be blocked.

If you forget your password or key, Telegram may offer recovery via:
- **Two-factor authentication**, or  
- **Verification on another device** (for example, your phone).


### Closing a secret chat (Desktop)

After leaving the chat or closing Telegram, you’ll need to re-enter the password or key the next time you access the chat.  


*Fictional instruction for training and documentation practice.*  
*Last updated: November 2025*
