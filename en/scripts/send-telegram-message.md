---
title: Send message to Telegram channel
desc: The command sends a message to the Telegram channel.
img:
   send-telegram-message: scripts/send-telegram-message.png
html:
   send-telegram-message: '<img src="%img.send-telegram-message%" style="margin: 1em 1em;"/>'
---
# Send Telegram Message

The **Send Telegram Message** command sends a text message to the specified Telegram channel using a bot.

%html.send-telegram-message%

**Bot API Token**  
Specify the API token of the bot that will send the message. The bot must be in the group of channel administrators and have the rights to post messages. For security reasons, it is not recommended to explicitly specify the bot token in this parameter.

``` txt
154149:AAEAro5-cFiWcIKXX5SsYoa3YE
#mybot#
```

**Channel Name or ID**.  
Specify the name of the public channel where the message will be sent. For example, *@mychannel*. If you are sending a message to a private channel, you must specify its ID. For example, *-10023673443*.

**Text**  
The text of the message to be sent.

**Exit on error**.  
Check this checkbox if you want to terminate the script execution in case of unsuccessful message sending. In this case, the error text will contain a response from the Telegram server.

## How to create a bot and a private Telegram channel

1. **Search for the “botfather”** telegram bot in the Telegram client.  
2. **Type /newbot** to create a new bot. You need to specify the bot's screen name and username. If the bot is successfully created, you will see the bot's API token like *356111742:cFiWcIKXX5SsYHDRDj34oa3YE*. You must not share this token with anyone.  
3. **Create a public channel** with a suitable name.
4. **Add your bot** to the list of administrators of the created channel. At least, the bot must have permission to post messages.

At this stage, you can already send messages to the created channel. If you want to make the channel private, you will need to get the channel ID first, as private channels cannot be accessed by name. To do that, specify the following address in the  browser **https://api.telegram.org/bot[API_TOKEN_BOT]/sendMessage?chat_id=[CHANNEL_NAME]&text=Test**, where *[API_TOKEN_BOT]* is the bot token, and *[CHANNEL_NAME]* is the channel name, for example *@mychannel*. If you've set everything right, you'll get an answer like this

``` txt
{ "ok":true, "result":{
     { "message_id":14,
     { "sender_chat": {
         { "id":-1001345116849,
         "title": "eonza", "type": "channel"},
     { "chat":{
         "id":-1001345116849,
         { "title": "eonza",
         { "type": "channel"}
     "date":1610522226,"text":"Test"
}}
```

The **id** parameter contains the channel identifier. After that, you can make the channel private and use this identifier instead of the channel name.
