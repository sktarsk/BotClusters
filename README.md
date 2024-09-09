<div align="center">
    <a href="https://github.com/MysteryDemon/BotClusters">
        <kbd>
            <img width="300" src="https://te.legra.ph/file/337898fcd33f27b9de71d.jpg" alt="Bot Clusters Logo">
        </kbd>
    </a>
</div>


## 🪧 ***BotClusters***

Have you encountered the problem where you have to host less resource intense Telegram Bots for free and you can only host a bot for an account but you wanted to host all bots in one instance, well say no more...

You can run multiple bots in a same instance, for now it only works for pure python bots (no docker support yet) but you need to host this on services which provide Docker support.

---

## ❓️ ***How to Use ?***

1. *Fork & Star this repository*
2. *Edit `config.json` to your Repo Data*
3. *Deploy and Host your Forked repository on server*
4. *Run Several Instance on Same Deploy*

---

<details><summary><b>Deploy To Koyeb</b></summary>
<br>
<b>The fastest way to deploy the application is to click the Deploy to Koyeb button below.</b>
<br>
<br>

[![Deploy to Koyeb](https://www.koyeb.com/static/images/deploy/button.svg)](https://app.koyeb.com/deploy?type=git&repository=https://github.com/sktarsk/BotClusters&branch=main&name=BotClusters)
</details>


## 🔰 ***Repo Features***

* **Stay Updated** since it clones from GitHub (on every Restart)
* **Extend** you can extend this to any number of bots by just adding more objects (see [Example](#example) below) although i recommend not to exceed 5 for 500 MB memory.
* **ENVs** you can set different ENV values for different bots even with same name.
* **Control** you can also set script file from where execution starts for that bot.
* **Private** you can also clone private repositories with help of Tokens. (see [Example](#example) below)
* **Web App** uses Flask to connect to service, so that it can be hosted as Dynamic Web Apps which is required for services like [Render](https://render.com/), [Koyeb](https://Koyeb.com/) etc.

---

## #️⃣ **Sample** `config.json`

1. **Bots Details**:

   `Ebook`: Indentifier Name (Can be Anything But Unique for Every Bot)

    |Variable|Value|Required|
    |:---:|:---:|:---:|
    |`source`|Give Github URL of it.|*Required|
    |`branch`|Branch of Github Repository|*Required|
    |`env`|Environment Variables for Bot|*Required|
    |`run`|Execution Command to run Bot|*Required|
    


```json
{   
    "Ebook": {
        "source": "https://github.com/bipinkrish/Ebooks-Bot.git",
        "branch": "main",
        "env": {
            "TOKEN": "xxx",
            "ID": "111",
            "HASH": "yyy",
            "REMIX_ID": "123",
            "REMIX_KEY": "abc123",
            "IA_EMAIL": "abcd@gmail.com",
            "IA_PASS": "pass@gmail.com"
        },
        "run": "main.py"
    },
    "Link": {
        "source": "https://github.com/bipinkrish/Link-Bypasser-Bot.git",
        "branch": "main",
        "env": {
            "TOKEN": "fff",
            "ID": "222",
            "HASH": "123abc"
        },
        "run": "app.py"
    },
    "Private": {
        "source": "https://bipinkrish:ghp_token@github.com/bipinkrish/private.git",
        "branch": "main",
        "env": {
            "TOKEN": "yyy",
            "ID": "444",
            "HASH": "abc321"
        },
        "run": "bot.py"
    }
}
```

---

### ℹ️ ***References:***

- `Source Repo` : [MultiBots](https://github.com/bipinkrish/MultiBots)
