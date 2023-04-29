<p align="center">
<img src="https://i.imgur.com/shFtqm7.png" alt="Logo">
</p>

[![GitHub](https://img.shields.io/github/license/SillyCodingBros/minecraft-status-bot?color=blue&style=for-the-badge)](License)

---

<details>
  <summary>Example</summary>

  <img src="https://i.imgur.com/ac1wj7n.png" align="center"/>

</details>

## Requirements

- [Docker](https://docs.docker.com/get-docker/)
- A [discord bot](https://discordapp.com/developers/applications/) token
- A Minecraft server (Example: **itzg**'s [Docker Minecraft Server](https://github.com/itzg/docker-minecraft-server))
- [Node.js](https://nodejs.org/en/download) (for development)

## Running from Docker Compose
    ---
    version: "3"
    services:
      minecraft-status-bot:
        container_name: minecraft-status-bot
        build:
          context: https://github.com/SillyCodingBros/minecraft-status-bot.git
          dockerfile: Dockerfile
        environment:
          - token=Disord_Bot_Token_Here
          - ip=Minecraft_Server_IP_Here
          - delay=Time_In_Milliseconds
        restart: unless-stopped

## Building & Running from source

    $ git clone https://github.com/SillyCodingBros/minecraft-status-bot.git
    $ cd minecraft-status-bot
    $ docker build -t minecraft-status-bot .
    $ docker run --name minecraft-status-bot -e "token=Disord_Bot_Token_Here" -e "ip=Minecraft_Server_IP_Here" -e "delay=Time_In_Milliseconds" minecraft-status-bot:latest

## License

This project is licensed under the MIT License - see the [License](License) file for details

## Acknowledgments

- Thanks to **AugusDogus**' [minecraft-status-bot](https://github.com/AugusDogus/minecraft-status-bot/) from which this project was forked.
