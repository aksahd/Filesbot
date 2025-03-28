

# requirements.txt
# >>>https://github.com/KurimuzonAkuma/pyrogram/archive/dev.zip
# >>>tgcrypto



from pyrogram import Client, filters, types
import logging

logging.BasicConfig(level=logging.INFO)
app = Client(
 name="Hotttzone_bot",
 api_id=25918813,
api_hash="d4c56885c14978cbf86205a09e60ed50",
 bot_token="7872286584:AAH6FKhuguB1IMF_FZm3IIbLFmL0JAZa7pQ"
      
)

chat_id: int = -7099681591
to_chat_id: int = -1918781172


@app.on_message(filters.chat(chat_id))
async def forward(bot: app, message: types.Message):
      # message.forward() is bound method of bot.forward_messages() 
      await message.forward(  # message.copy() for without tag.
      
              to_chat_id
      )


app.run()
