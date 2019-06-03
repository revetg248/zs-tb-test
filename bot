import telebot
bot = telebot.TeleBot("518538771:AAGJoGfapbrr4VA4NIAUztl3ToWNk-H5dpQ")
print(bot.get_me())
def log(message, answer):
    from datetime import datetime
    print('\n ------')
    print(datetime.now())
    print("Сообщение от {0} {1}, (id ={2}) \n Текст -{3}".format(message.from_user.first_name,
                                                                   message.from_user.last_name,
                                                                   str(message.from_user.id),
                                                                   message.text))
    print(answer)
@bot.message_handler(commands=['help'])
def handle_text(message):
    user_markup = telebot.types.ReplyKeyboardMarkup(True, False)
    user_markup.row('test', 'test2')
    answer = "Мои возможности ограничены. Sorry!"
    log(message, answer)
    bot.send_message(message.chat.id, answer, reply_markup=user_markup )
bot.polling(none_stop=True, interval=0)