darmen_proxy


==========




Исходный код 
----------
```python

# импортируем нужные библиотеки
from aiogram import Dispatcher, types, Bot
from aiogram.utils import executor
import random
# твой токен который ты получишь после создания бота у @BotFather
TOKEN = '5653921692:AAHiyjtA10OBzQEr-9iy-ktFk-64eTHYAmY'

# объекты бота
bot = Bot(TOKEN)
dp = Dispatcher(bot)

# функция которая будет          

@dp.message_handler(commands="url")
async def cmd_inline_url(message: types.Message):
    buttons = [
        types.InlineKeyboardButton(text="TikTok", url="https://www.tiktok.com/@darmen_3?_t=8V86h2u1KmT&_r=1"),
        types.InlineKeyboardButton(text="Инста", url="https://instagram.com/darmen_proxy?igshid=YmMyMTA2M2Y="),
        types.InlineKeyboardButton(text="Twitch", url="https://www.twitch.tv/father_darmen3?sr=a"),
       
        types.InlineKeyboardButton(text="Оф. канал Telegram", url="https://t.me/+ZNzxmC1FV51iYWRk")#
        
        
    ]
    keyboard = types.InlineKeyboardMarkup()
    keyboard.add(*buttons)
    await message.answer("Соц сети 🏴‍☠️", reply_markup=keyboard)


    
    
   
            
@dp.message_handler(commands="sticker")
async def bot_start(message: types.Message):  # Любая асинхронная функция
    # ...
    r=random.choice(["CAACAgIAAxkBAAEFrTVjB8kqqa5o6RDtte8VKJueROP41QACUB0AAmsrQUg5vcjtVWGJZSkE","CAACAgIAAxkBAAEFrTdjB8kurgI4pM30p0kg4xHr-tjUUwACyh8AAps1OEgEwoYUYltEhCkE","CAACAgIAAxkBAAEFrTljB8kwiwZ3weKDqHIkZzZJSNx3rgACOh0AAo62QUhp0Dyw925JmykE","CAACAgIAAxkBAAEFrTtjB8kyeNcbtunWBr_wayOJoJ9vjQACkhsAAgJAQEihJsOsaz-QGSkE","CAACAgIAAxkBAAEFrT1jB8k0iFK9k0l52YCLnVoOkMpJwQACXiEAArF6OUj-uEDMcXvLyikE","CAACAgIAAxkBAAEFrT9jB8k28mamW4gMLxY7yvYtkVSFIwACEh0AAiKAOEgFoYFLgy_7xCkE","CAACAgIAAxkBAAEFrUFjB8k4u5rWh9t2gmV0dowghI-5-gAC4x0AAtYuOEgRPV3sqo5H-ikE","CAACAgIAAxkBAAEFrUNjB8k64GWtdBQyeUCYe9Ak0VJJJAACTx8AAiIAAUFIoOBhT3UciH4pBA","CAACAgIAAxkBAAEFrUVjB8k8xzj0vso6zrVCXBoR6OwVcAACDBsAAv-DQEiYH4oieudrwSkE","CAACAgIAAxkBAAEFrUdjB8k-hK19n9WdFHqmwo70u-g5twACbR4AAo-SOEie-TQlQ0X2GCkE","CAACAgIAAxkBAAEFrUljB8lAgOKbSTLFZZ2t4RNlO8PJnQAC3BkAAg9iQEhXJmlqCueF9SkE","CAACAgIAAxkBAAEFrU1jB8lEtYQflGZLCwjlnDnbhinTUwACYR4AAuURQEgbIK1kQBSlvikE","CAACAgIAAxkBAAEFrVFjB8lI_AMki_qgtuI3q-ycDIj9rgAC2yAAAsL3OEi7om-xsHGelCkE","CAACAgIAAxkBAAEFrVNjB8lK04-rHuR1taPE-7swnGV_GAACox8AAlcrQUh0ULXrcdB5VSkE","CAACAgIAAxkBAAEFrVdjB8lOsUgCnqmFzWWB8hPLFo7U3AACUyQAAhiYOUgWy4RSf7VBBSkE","CAACAgIAAxkBAAEFrVtjB8lT_Dgf7YbYYV3eHY21YJiomwACkiYAAqqlQUir93_smGF9UykE","CAACAgIAAxkBAAEFrkpjCJQyn52uWAMDVJWO69wBGlulyQACGiAAArm_QUh64clNukGbvCkE","CAACAgIAAxkBAAEFrk5jCJQ2-Q1k0M9Yu-F95p4vF_MjDQACdSEAArPPQUgjhQfqMd2G9SkE","CAACAgIAAxkBAAEFrlFjCJQ41P3l2_nYGrIsjdgo_nTf2gACkyAAAq3fQUhzxL22vrsXFSkE","CAACAgIAAxkBAAEFrlRjCJQ6NyLnIpOhFVP2wDJOvuyjGgAChR0AAlpFQUiQ5pcvadOE4SkE","CAACAgIAAxkBAAEFrlZjCJQ9G0YH8v-dy8oh7kzgHHv2CgACBiMAApakOUijAezxt_0t7ikE","CAACAgIAAxkBAAEFrlxjCJRAb4D69rO5oL3_DEC7q3BcDQACWyMAAipAQUjCwvInsjSZVCkE","CAACAgIAAxkBAAEFrl5jCJRCpcmD6pkQWDAJ6BEMHdp2xQACmyIAAt5MQEiwtUjju0vrbykE","CAACAgIAAxkBAAEFrmJjCJRJOWZFKmxfgWnQvAaj0_jVugACTh4AAqbNQEi_2m0U0dI96SkE","CAACAgIAAxkBAAEFrmRjCJRMwdbfgokBS5sNEcrnWjxYewACRx8AAsqhQUgg44yjIDxFgikE","CAACAgIAAxkBAAEFrmZjCJRNLIj98cH2OwRyiEfKHBY_RwAC2CIAApUEQEhX6RyaGAxP8SkE","CAACAgIAAxkBAAEFrmhjCJRQspN0qiPZXJ1bGtEyPICsUgACpiIAAmjXOEjWZalSJPOCzCkE","CAACAgIAAxkBAAEFrmpjCJRRFKaxhqW45fqolOpyirBoUgACpCEAApmNQEiX60G0X5C7xikE","CAACAgIAAxkBAAEFrmxjCJRTes0sqMa5Km4-kSyzIG8N7QACNx0AAjioQEhP0S6Hjx5rwykE","CAACAgIAAxkBAAEFrm5jCJRVnyF1kUSWTG6izY2NuX1vnQACxB8AAi45QEjZWgo0DmHt7ikE","CAACAgIAAxkBAAEFrnBjCJRYW7otVy9Jh1OycKhCYletMgACUxwAAleHQUiKij8ieA3S6CkE","CAACAgIAAxkBAAEFrnJjCJRak87iDtoEnnC-YAmNXpMrxgACSyMAAlIoQUhRKBCrz34GaykE"])
    await message.answer_sticker(
                           sticker=r)
                           

@dp.message_handler(commands = ['gif'])
async def mai(message: types.Message):
    # строка, чтобы отправить что-нибудь в групп
    
    	koks=random.choice(["https://i.gifer.com/3769.gif","https://i.gifer.com/DaN.gif","https://www.icegif.com/wp-content/uploads/one-piece-icegif-3.gif","https://i.gifer.com/2mkS.gif","https://i.gifer.com/62H9.gif","https://i.gifer.com/91Rt.gif","https://i.gifer.com/3769.gif","https://i.gifer.com/1FiZ.gif","http://24.media.tumblr.com/tumblr_lwf0ea2DOu1qabxyjo1_500.gif","http://pa1.narvii.com/6495/9c3b145a8c23e92c70b6980abf0501abac2ce97f_00.gif","https://38.media.tumblr.com/tumblr_m5gd78rX9C1r18y5qo1_500.gif","http://25.media.tumblr.com/tumblr_m4utprWpNE1r18y5qo3_500.gif"])
    	await message.answer(f"{'<b>'}one-piece🏴‍☠️\n\n{koks} {'</b>'}", parse_mode = 'HTML')        
    	
@dp.message_handler(commands = ['darmen3'])
async def mai(message: types.Message):
    # строка, чтобы отправить что-нибудь в групп
    
    	koks=random.choice(["CAACAgIAAxkBAAEFroJjCKihg-16_TsaSFVi_6Ix1VNmqgACdxcAAoLaUUhszISopa_COSkE","CAACAgIAAxkBAAEFroRjCKinsBsNca7EF6QnAZWhDimHtgACIxwAAhvWSUi15gABkl7NKIcpBA","CAACAgIAAxkBAAEFroZjCKiphbEV_XbHhk3W5q6Jj5OwVAACgRkAAv_CSEgEIfJJvs9qcSkE","CAACAgIAAxkBAAEFrohjCKisBqTuDr3yrhnK0mg0Y5HRQwACqBsAAlGSSEgcB29wiSrzFykE","CAACAgIAAxkBAAEFropjCKiuwtrxiRQ3TEAAASesEbbI7woAAhMbAAJ1RVFIPCd2qoAZPC8pBA","CAACAgIAAxkBAAEFroxjCKiwtjR9-mgHiRWpjAed7fdPBQACrxwAAu7lSUgrDkz2z944nSkE","CAACAgIAAxkBAAEFro5jCKizVHH8w8fGr78cQiCrDAEGGgACCxcAAhKsUEiO4BvTinfNsSkE","CAACAgIAAxkBAAEFrpBjCKi1oqm_OeNzJs-qxavF6npzVwACpRkAAjS-SUiDKZNJonuLHCkE","CAACAgIAAxkBAAEFrpJjCKi3MkM-PiFGg_6LDNsB7hbExAACghgAApKqSEh0gkFB0LrPUikE","CAACAgIAAxkBAAEFrpRjCKi8IgVFnVY7crO8ILrm532KtwACdxcAAoLaUUhszISopa_COSkE","CAACAgIAAxkBAAEFrpZjCKi_f6ZEI-8ZEUbU_DVqpHTvowACcRwAAqe9SUhaDt4PR-n4SikE","CAACAgIAAxkBAAEFrphjCKjB-by1V-Ma2ihEk78Qgxs9cgACNRkAAgzPSUhrvgVPzNgKmSkE","CAACAgIAAxkBAAEFrppjCKjp-k5_gyIJssE04mugHnI_DwACxioAApAsSUidWKVuG8sSYCkE","CAACAgIAAxkBAAEFrpxjCKjrX2jM25mbdH2OKWFgOnnTYAACBh8AArdkQUh24Wu_Qjj4VykE","CAACAgIAAxkBAAEFrp5jCKjt06Y41UpSSDvZJ9y6IBJDowACaBwAAjNvSUgy9GdkrfX1gSkE","CAACAgIAAxkBAAEFrqBjCKjwdAoT5Y2u_v80WvxWeU-2QQAC1RsAAorzSEjxmjZoBcShVCkE","CAACAgIAAxkBAAEFrqJjCKjxvPVo_wbmHW2Ps926ZvDYOQACMSEAAqWuQEgoPEglhS2hICkE","CAACAgIAAxkBAAEFrqRjCKj0ndcKR1JmuSR4X2fcHAI8kQACrR0AAklpQUivQEwKNOplvCkE","CAACAgIAAxkBAAEFrqZjCKj2CrDC11gIMbnuNQ88D_PBewAC8xoAAtsDSUjIdafHXWfMJykE","CAACAgIAAxkBAAEFrqpjCKwmjbOEKnRfdOsSPAFV92717gACyR8AAr9nSUgXp-sAAQNCqP8pBA"])
    	await message.answer_sticker(
                           sticker=koks)       	      
    	                  
@dp.message_handler(commands = ['chopper'])
async def mai(message: types.Message):
    # строка, чтобы отправить что-нибудь в групп
    await message.answer_sticker(
                           sticker=random.choice(["CAACAgUAAxkBAAEFruhjCM1Jwy-pAAFeC0k2ypxVgF0BpewAAuoBAAJPBZhUTFYM2oHpl6wpBA","CAACAgUAAxkBAAEFrupjCM1MqOsmIqjedW5kpkjBGaq7ggACqQIAAihYmVQdrTurAW5WUykE","CAACAgUAAxkBAAEFruxjCM1Po7DDq0djU7NICj2LpPT2XwACKQIAAsCemVTJWyKZR-RwRykE","CAACAgUAAxkBAAEFru5jCM1Rb6aLi3Lrdh3027BuPXex3gACGwIAApXooFT9PHQ2pURH7ykE","CAACAgUAAxkBAAEFrvBjCM1TfMHMYhV5GqCkHoToZBC5GAAC2wEAAuSNmFS_KyUIwD52iSkE","CAACAgUAAxkBAAEFrvJjCM1VZM4JPjoLFXbPu9blMvqg5wACagEAAuhtmFQuqNCoLY_yxykE","CAACAgUAAxkBAAEFrvRjCM1XOxtNzdTGDhav6t01xYke3AACQQIAAvANmVR38gZYc0V_kikE","CAACAgUAAxkBAAEFrvZjCM1ZyPJe7xGaVK2SlHn0cwzGdQACwwEAAmfDmVQXqouE_70zKSkE","CAACAgUAAxkBAAEFrvhjCM1bQxeAqQABhftvx36_YgnWVxEAAv0BAALa1qFU2MkI-810FrApBA","CAACAgUAAxkBAAEFrvpjCM1djfR8USgqwX4iCoXx3sswHgACogIAAvykmVQJHA7sIGttSykE","CAACAgUAAxkBAAEFrv5jCM1mKXgHMaLkgxBOTId099CD9AACGgIAAknPmFQMM_1iVunMeCkE","CAACAgUAAxkBAAEFrwABYwjNaFPEiyo0JM2BaAgNzVQPuiAAAgECAAKn-qFUEv-mlfgls18pBA","CAACAgUAAxkBAAEFrwJjCM1qkv2WNdBPCCWHRs8sawTz9QAChgEAAgt6mFSJ26DJBHETyikE","CAACAgUAAxkBAAEFrwRjCM1sC2gLiTe9MBmX-RKXSmCSuwAC3AEAAoOSoFQv6Ie9czkoMikE","CAACAgUAAxkBAAEFrwZjCM1uD_-RDbCmsTlch2Or_LoHowACTQIAAk9ToFQd5B1GMET-DCkE","CAACAgUAAxkBAAEFrwhjCM1xUgABKv-21sxNuuKJcG8iHBQAArMBAALT7aFU8715x9NtAUApBA","CAACAgUAAxkBAAEFrwpjCM1zWXor6SYCqEFoCmVhNCT5GwACvwIAAlK4mFRaA9s0c_9QmikE","CAACAgUAAxkBAAEFrwxjCM118TdQ5czea0yPt11whP8DKAACqAEAAr-SmVRIzzhdVKYAAdEpBA","CAACAgUAAxkBAAEFrw5jCM13QLaEabcUUD_2DEUzlBKxrAACdAEAAqp3oVRgzZEzlpfMUykE","CAACAgUAAxkBAAEFrxBjCM15MKM9h0wtts3NI8kmq7zBFwAC1gEAAlSlmFSslCy9fhokDSkE","CAACAgUAAxkBAAEFrz1jCNjfOY8wx9zMib2zH9vGrTqgpgACsQEAAmiSmFSwvy6gYub0UykE","CAACAgUAAxkBAAEFrz9jCNjiDwtpOi95bDLYS6RtCnKbcQAC3wEAAuGcmFRFJUfGuvRB_CkE","CAACAgUAAxkBAAEFr0FjCNjkDKsDwh5dc7zkgkjv5Gsy6wACnwIAAi5kmVSj7JKCngABhxEpBA","CAACAgUAAxkBAAEFr0NjCNjmhmuxgxRGVIs2uwg51SZqVgAC1QIAAjW4mVRVHNDmetRrKykE","CAACAgUAAxkBAAEFr0VjCNjrATloJwZKRuPR6W_7L5Rk3QACjwEAAhVsmVQGFo4qnyWnxSkE","CAACAgUAAxkBAAEFr0djCNjtpGfC2JLlrX5XTSiUMd6esAACngEAAl2bmFQ4pI6B_cUdFCkE","CAACAgUAAxkBAAEFr0ljCNjvYSm_v_-5MTbZc4r-5VTjOgACzgIAAuzXmVQEu6XpD_8pPykE","CAACAgUAAxkBAAEFr0tjCNjwmwW6Fis_YQVdRpjGnvepCQACWgIAAmUCmVQU0UU4H98t9SkE","CAACAgUAAxkBAAEFr01jCNjzP5ON9Us-KfLhMHSH5GIF3wACxQIAAtAVmVSkU7JGs9MqrCkE","CAACAgUAAxkBAAEFr09jCNj1NYIn1Phu2b5kcP8JBVtdtgACrwEAAgL8oVSh0TPuWZgzgSkE"]))

                                  
# запускаем бота
print("Отец на связи")
executor.start_polling(dp)

"""
Код будет обновляться но не сейчас (жду указание отца)
"""

```
