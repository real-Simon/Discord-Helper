# At first

i thank to [melion](https://discord.com/invite/melion) (German Server)

## Set Up

```Python
builder = HelpCommandCreator(title="The Title of the Embed", description="description of the embed", color=discord.Color.random(), inline=True)
```
All arguments aren't required, but you can use them to customize your embed. 
if color is None the color is a random color, and inline is False if not set.

## Add command

to add a command just use 
```Python
builder.add(name="command-name", description="command-description")
```

both arguments are required.

## Send the Help command

```Python
@bot.command()
async def help(ctx):
    await ctx.send(embed=builder.create_help_embed())
```

## Final

if you use this example code:
```Python
import discord
client = discord.Client()
builder = HelpCommandCreator(title="**Help** for ME!", description="See my help here")

builder.add("!test", "testcommand")
builder.add("!ban", "not available")
builder.add("!help", "get this help displayed")
@client.event
async def on_message(message):

    if message.content.startswith("!test"):
        await message.channel.send("Test command")

    if message.content.startswith("!ban"):
        await message.channel.send("not available")

    if message.content.startswith("!help"):
        await message.channel.send(embed=builder.create_help_embed())

client.run("token")
```
it must work, if u get errors just say it to me (Simon.py#3306)

## Download
Just download the file, and drag it to your main file. Then just import it. 

