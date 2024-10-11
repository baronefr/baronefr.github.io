---
title: "Hermes"
excerpt: "Telegram bot for messages, task notifications & system management."
collection: things
gitlink: 'https://github.com/baronefr/hermes'
date: 2024-10-10
---

<br>
<img src='https://raw.githubusercontent.com/baronefr/hermes/master/img/cover.png' style='width:100%;max-width:700px;display:block;margin-left:auto; margin-right:auto;'>


## What is Hermes?

Hermes is a Python library that provides a Telegram bot interface for your computer.
It is capable of sending messages, files, or images to a specific user, either via terminal commands or inside Python scripts.
Additionally, it can run as a server that interacts with specific commands received through the Telegram bot. 


In detail, the functionalities of Hermes are developed around three core blocks:
* **CLI**
    - send a text message
    - send images and files
    - send a message after the completion of a specific command/process (which can be carried out in background)
* **Bot server** - A user can interact with the bot to execute specific commands:
    - poweroff/reboot your system
    - retrieve power statistics
    - retrieve network status
    - *custom functions* implemented by the user
* **Tasks**
    - create a Python script using the Task module of Hermes, in order to ...
        - ... receive notifications (waypoint-based) to keep track of the script execution
        - ... send images and Matplotlib plots through the bot
        - ... create a private log file that can be retrieved through the bot server
    - failsafe: an error in Hermes does not stop your code

<br>

### Requirements

* Linux system
* Python 3.8 or above
    - the following packages are required: `pyTelegramBotAPI termcolor`

<br>

## [Documentation](https://bothermes.readthedocs.io/en/latest/)

I tried to include as much as possible in the [package documentation](https://bothermes.readthedocs.io/en/latest/). Follow through the **Setup** section to install and configure Hermes. The rest of the documentation should help with the usage.
