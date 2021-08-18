import discord


class HelpCommandCreator:
    def __init__(self, title: str = "Help command for this Bot", description: str = "Help for me!",
                 inline: bool = False, color=None):
        if color is None:
            color = discord.Color.random()
        else:
            color = color
        self.color = color
        self.liste = []
        self.title = title
        self.description = description
        self.inline = inline

    def add(self, name: str, description: str):
        self.liste.append([name, description])
        pass

    def create_help_embed(self):
        embed = discord.Embed(title=self.title, description=self.description, color=self.color)
        c1 = 0
        for i in self.liste:
            embed.add_field(name=i[c1], value=i[c1 + 1], inline=self.inline)
        return embed
