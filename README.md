A Discord bot built with Python 3 that delivers trivia questions and evaluates the correctness of answers, using `discord.py`. The bot also manages a profile for each server member for various question categories.

**Instructions**
1. Clone or fork this repository and make sure you have the files locally
2. Create your own bot account and invite the bot to your server (refer to the [Discord documentation](https://discordpy.readthedocs.io/en/latest/discord.html) for specific instructions)
3. At [discord.com/developers/applications](https://discord.com/developers/applications), click on your new bot/application
4. Under Settings, click on Bot
5. Copy the bot token
6. Open the .env file and paste your bot token on line 2, after DISCORD_TOKEN=
7. In terminal, run:  `python TriviaBot.py`

That's it! The bot should be ready, and you can give it commands by typing in a message that begins with an exclamation mark. For example, try typing `!help` for a list of possible commands.

**Dependencies**    
`discord.py`  
`dotenv`  
`asyncio`  
`pandas`  
`os`  
`json`  
`random`  
`shutil`  

**Files**  
1. `TriviaBot.py`: main code that uses concurrent programming with `discord.py` to listen and respond to commands  
2. `manage_questions.py`: contains the `Questions` class that imports questions, returns individual questions, and save question order on disconnect  
3. `trivia_questions_guild_*.csv`: contains last saved list of questions for a guild  
4. `bot_responses.json`: contains responses that bot could use for different situations
5. `current_state.json`: contains current question, answer, category, and scores for players. Using a dictionary allows bot to retrieve scores by looking up the guild ID then member ID in constant time
6. `developers_id_list.txt`: contains IDs of all users who are allowed to use the `!disconnect` command to disconnect the bot
