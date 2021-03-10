# Server Status - Website
**A real time server status plugin**

*Note: this site is still a WIP and very subject to change*

## Backend
The basis of this project is a webserver. This webserver runs *Socket.io*, a wrapper around and implementation of websockets. The webserver communicates to the plugin and web-clients to distribute real time server information. When the webserver recieves a packet from the Minecraft plugin it immediately routes the information to clients on the web and on discord.

## Frontend
The frontend of this site dynamically displays the information it receives from the webserver. It has a small indicator, either red or green, to display the current status of the Spigot server. Additionally it shows the player count of people online and lists their avatars *(you can view their names on hover)*. There is also a simple text-only version of the site that dynamically updates at `/simple` and an api which returns the current status statically at `/api`.

## Installation
To install this webserver it's required that you have node.js and npm installed on your system. To install all required dependencies run `npm install` in the main directory, and to start it run `npm start`!

## Configuration
Don't want your web server running on the default port? No problem! The configuration file located at `config.yml` lets you customize which port your server runs at in the `port` field. It also allows you to add a custom name for your site visible in the title of the webpage as well as in the header in the middle with the `name` field. As this plugin doesn't currenrly query your server for its max player count, set the visible max players of your server in `max_players`. Finally, if you don't want the background of your site to be play, set a background image in the `background_img` field! To get your changes to take effect, restart the webserver with `npm start`.

### Default configuration:
```
# Port for the web server to run at
port: 80

# Name of the site
name: 'Minecraft Server'

# Server's max players
max_players: 20

# Background image for the site (optional)
# To remove set to ''
background_img: ''
```
