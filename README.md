# Myso1
#Помогает понять человеку как нужно правильно выкидывать, следить за мусором
import discord
from discord.ext import commands 

intents = discord.Intents.default()
intents.message_content = True

bot = commands.Bot(command_prefix='-', intents=intents)

@bot.command()
async def info(ctx):
   await ctx.send(f' Учёные провели эксперимент и доказали, что бумажный фантик, находясь в земле в течении 3-х недель размокает и почти полностью разлагается. А фантик из фольги почти не пострадал. Среднее время разложения пластмассовых изделий, созданных по разным технологиям, колеблется от 400 до 700 лет. Полиэтиленовые пакеты, которые повседневно используются людьми, в природе разлагаются от 100 до 200 лет. Это обратная сторона прочности и долговечности пластиковых изделий. При этом стеклянная бутылка может разлагаться до 1 млн лет.По данным научных статей пластиковая бутылка разлается примерно 450 лет, одноразовый подгузник - 500 лет. Многие виды пластика не разлагаются вовсе. ')
    

@bot.command()
async def Plastikimage(ctx):
    with open('image/slide-4.jpg', 'rb') as f:
        # В переменную кладем файл, который преобразуется в файл библиотеки Discord!
        picture = discord.File(f)
   # Можем передавать файл как параметр!
    await ctx.send(file=picture)

@bot.command()
async def bymaga(ctx):
    with open('Bymaga/help.jpg','rb') as f:
        picture = discord.File(f)
    await ctx.send(file=picture)
@bot.command()
async def Batareika(ctx):
    with open('batareika/batareki.jpg', 'rb') as f:
        # В переменную кладем файл, который преобразуется в файл библиотеки Discord!
        picture = discord.File(f)
    # Можем передавать файл как параметр!
    await ctx.send(file=picture)

def get_random_meme():
    meme_folder = "batareika/abatareki"
    
    # Получаем список файлов из папки
    meme_files = os.listdir(meme_folder)
    
    if meme_files:
        # Выбираем случайный файл из списка
        meme_file = random.choice(meme_files)
        meme_path = os.path.join(meme_folder, meme_file)
        
        return meme_path
    else:
        return None




bot.run("Тут ваш токен")
