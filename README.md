
<p float="left">
<img src="https://img.shields.io/github/languages/top/fredhappyface/Python.IRCBot.svg?style=flat-square" alt="Github top language">
<img src="https://img.shields.io/codacy/grade/40723caf8eff4be8bad8dd6f1213f82a.svg?style=flat-square" alt="Codacy grade">
<img src="https://img.shields.io/codacy/coverage/40723caf8eff4be8bad8dd6f1213f82a.svg?style=flat-square" alt="Codacy coverage">
<img src="https://img.shields.io/github/repo-size/fredhappyface/Python.IRCBot.svg?style=flat-square" alt="Repository size">
<img src="https://img.shields.io/github/issues/fredhappyface/Python.IRCBot.svg?style=flat-square" alt="Issues">
<img src="https://img.shields.io/github/license/fredhappyface/Python.IRCBot.svg?style=flat-square" alt="License">
<img src="https://img.shields.io/github/commit-activity/m/fredhappyface/Python.IRCBot.svg?style=flat-square" alt="Commit activity">
<img src="https://img.shields.io/github/last-commit/fredhappyface/Python.IRCBot.svg?style=flat-square" alt="Last commit">
</p>


# Python.IRCBot

<img src="readme-assets/icons/name.png" alt="Project Icon" width="750">

Use sockets to attempt to join an IRC channel and talk with a bot


## Download
### Clone
#### Using The Command Line
1. Press the Clone or download button in the top right
2. Copy the URL (link)
3. Open the command line and change directory to where you wish to clone to
4. Type 'git clone' followed by URL in step 2
```bash
$ git clone https://github.com/[user-name]/[repository]
```

More information can be found at
<https://help.github.com/en/articles/cloning-a-repository>

#### Using GitHub Desktop
1. Press the Clone or download button in the top right
2. Click open in desktop
3. Choose the path for where you want and click Clone

More information can be found at
<https://help.github.com/en/desktop/contributing-to-projects/cloning-a-repository-from-github-to-github-desktop>

### Download Zip File

1. Download this GitHub repository
2. Extract the zip archive
3. Copy/ move to the desired location


## Language information
### Built for
This program has been written for Python 3 and has been tested with
Python version 3.7.0 <https://www.python.org/downloads/release/python-370/>
on a Windows 10 PC.
### Other versions
To install Python, go to <https://www.python.org/> and download the latest
version.
## How to run
1. Open the .py file in IDLE
2. Run by pressing F5 or by selecting Run> Run Module



## What this program does
- Read configuration data from a json file ('data.json'). In the form:
```json
{
"host_url": "irc.hostname.org",
"protocol": "IRC",
"port": 6667,
"irc_channel": "#channel",
"bot_name": "bot_name",
"user_name": "user_name",
"user_password": "user_password"
}
```
- Gets a message in its raw from
```python
getRawMessage()
```
- Takes a raw message and refines it (name, message)
```python
getRefinedMessage(messageData)
```
- Starts an IRC connection, signs in and goes to the desired channel
- Ignore the welcome messages


## Add your own application code
You can add code to talk to the target bot
deal with any responses and deal with them appropriately. For instance you may
want to implement a 'chatbot' or answer challenge questions (in the case of
root-me)

## Example code

Send a private message to our target bot
```python
irc.send(bytes("PRIVMSG "+ bot_name +" :"+ "my message here" +"\n", "UTF-8"))
```


Get a message from the bot
```python
messageData = getRawMessage()
if (DEBUG):
    print(messageData)
name, message = getRefinedMessage(messageData)
print(name, message)
```


## Licence
MIT License
Copyright (c) fredhappyface
(See the [LICENSE](/LICENSE.md) for more information.)
