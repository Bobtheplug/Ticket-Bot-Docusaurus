---
sidebar_position: 3
---

# Configuration

First you need to set the token of your bot in the `token.json`.  
Example:

```json
// config/token.json
  "token": "my.discord.bot.token"
```

To configure Ticket Bot, you need to edit the `config.jsonc` file in the `/config` folder.

```json
// config/config.json
  "clientId": "123456789123456789", // The id of the discord bot
  "guildId": "123456789123456789", // The id of the discord server
  "mainColor": "f6c42f", // The hex color of the embeds by default
  "lang": "main", // If you want to set english please set "main"


  "openTicketChannelId": "897568683394752523", // The id of the channel where the message to create a ticket will be sent
  "ticketTypes": [ // You have a limit of 25 types (the limit of Discord)
    {
      "codeName": "suggestion", // The name need to be in lowercase
      "name": "Suggestion", // The name that will be displayed in the ticket
      "emoji": "💡", // The emoji of the type (can be blank)
      "color": "#e45671", // Can be a hex color or blank to use the main color
      "categoryId": "123456789123456789", // The category id where the tickets will be created
      "customDescription": "Please explain your suggestion in detail. If you have any images, please attach them to your message.\n\nReason: REASON", // The custom description of the ticket type (set to blank to use the default description)
      "askReason": true // If the bot should ask the reason of the ticket
    },
    {
      "codeName": "report", // The name need to be in lowercase
      "name": "Report", // The name that will be displayed in the ticket
      "emoji": "🛑", // The emoji of the type (can be blank)
      "color": "#f8312f", // Can be a hex color or blank to use the main color
      "categoryId": "123456789123456789", // The category id where the tickets will be created
      "customDescription": "Please explain your report in detail. If you have any images, please attach them to your message.\n\nReason: REASON", // The custom description of the ticket type (set to blank to use the default description)
      "askReason": false // If the bot should ask the reason of the ticket
    },
    {
      "codeName": "other", // The name need to be in lowercase
      "name": "Other", // The name that will be displayed in the ticket
      "emoji": "", // The emoji of the type (can be blank)
      "color": "", // Can be a hex color or blank to use the main color
      "categoryId": "123456789123456789", // The category id where the tickets will be created
      "customDescription": "", // The custom description of the ticket type (set to blank to use the default description)
      "askReason": false // If the bot should ask the reason of the ticket
    },
  ],
  "ticketNameOption": "Ticket-TICKETCOUNT", // Here is all parameter: USERNAME, USERID, TICKETCOUNT
  "rolesWhoHaveAccessToTheTickets": [
    "966046902493806642",
    "897570577857011752"
  ], // Roles who can access to the tickets
  "pingRoleWhenOpened": true,
  "roleToPingWhenOpenedId": "966046902493806642", // The role to ping when a ticket is opened
  "logs": true,
  "logsChannelId": "966046987738816552", // The id of the channel where the logs will be sent
  "claimButton": true,
  "whoCanCloseTicket": "STAFFONLY", // STAFFONLY (roles configured at "rolesWhoHaveAccessToTheTickets") or EVERYONE
  "closeButton": true, // If false the ticket can be closed only by doing /closes
  "askReasonWhenClosing": true, // If false the ticket will be closed without asking the reason
  "maxTicketOpened": 1 // The number of tickets the user can open while another one is already open. Set to 0 to unlimited
}
```

## Change some embeds

If you want to change some embeds, you can edit the json of locales in the `/locales` folder. By default the bot use `main.json` but you can edit it to use another language.
