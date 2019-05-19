IRC Bot Config for Freenode (#SecurityFeed)

Bot source: https://github.com/impredicative/irc-rss-feed-bot

This bot posts content from various security oriented feeds.

If you wish to add a RSS feed just create a request.

:-)


**Docker Compose**

```
  ircbot:
    container_name: ircbot
    hostname: ircbot
    image: ascensive/irc-rss-feed-bot:0.3.2
    restart: always
    logging:
      options:
        max-size: 10m
        max-file: "3"
    volumes:
      - /docker/ircbots/securityfeed/config:/config
    env_file:
      - /docker/ircbots/securityfeed/secrets.env
```
