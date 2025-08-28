[bot.py](https://github.com/user-attachments/files/22017447/bot.py)
import discord
TOKEN = "MTQxMDE1MDk0NTk5NTYyNDYwNA.GaP0rs.11GbWRaDNBnpBhVLRi93dZtAYtlyqw2msGdA4E"
client = discord.Client(intents=discord.Intents.all())
@client.event
async def on_ready():
    print(f'We have logged in as {client.user}')
@client.event
async def on_message(message):
    if message.author == client.user:
        return
    if message.content == '/自由民主党':
        await message.channel.send('国会内の比較第一党。 総裁は石破茂 (総理) 自由民主主義の理念を掲げている 政治的立場 中道右派 最大与党')
    elif message.content == "/立憲民主党":
        await message.channel.send("代表は野田佳彦(元総理) 立憲民主主義の理念掲げている 国会内の比較第二党。 政治的立場 中道左派 最大野党")
    elif message.content == "/日本維新の会":
        await message.channel.send("行政改革や憲法改正、 規制改革、 機会平等、 地方分権などを政策に掲げる 代表は吉村洋文 (共同代表は藤田文武 ) 政治的立場 中道右派")
    elif message.content == "/国民民主党":
        await message.channel.send("立憲保守からリベラルまでを包摂する 代表は玉木雄一郎 政 治的立場 中道")
    elif message.content == "/公明党":
        await message.channel.send("宗教団体の創価学会を支持母体として中道政治の実現を目指して結成 された。 代表は斎藤鉄夫 1999年10月5日から2009年9月16日まで、 および2012 年12月26日から現在まで自由民主党と自公連立政権を構成している政権与党。 政治的立場 中道")
    elif message.content == "/参政党":
        await message.channel.send("「日本の国益を守り、 世界に大調和を生む」 という理念を掲げている 政治的立場 右派 代表は神谷宗幣")
client.run(TOKEN)
