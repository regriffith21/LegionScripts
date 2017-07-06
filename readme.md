<h1 align="center">LegionScripts - Installation Instructions</h1>

<div align="center">
  :steam_locomotive::train::train::train::train::train:
</div>
<div align="center">
  <strong>Quality Jackpot website for ⅕ the price!</strong>
</div>
<div align="center">
  Built with <code>nodejs</code> & <code>php</code>
</div>

<br />

<div align="center">
  <!-- Stability -->
  <a href="https://nodejs.org/api/documentation.html#documentation_stability_index">
    <img src="https://img.shields.io/badge/stability-experimental-orange.svg?style=flat-square"
      alt="API stability" />
  </a>
  <!-- Build Status -->
  <a href="https://travis-ci.org/yoshuawuyts/choo">
    <img src="https://img.shields.io/travis/yoshuawuyts/choo/master.svg?style=flat-square"
      alt="Build Status" />
  </a>
  <!-- Test Coverage -->
  <a href="https://codecov.io/github/yoshuawuyts/choo">
    <img src="https://img.shields.io/codecov/c/github/yoshuawuyts/choo/master.svg?style=flat-square"
      alt="Test Coverage" />
  </a>
  <!-- Standard -->
  <a href="https://standardjs.com">
    <img src="https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat-square"
      alt="Standard" />
  </a>
</div>

<div align="center">
  <h3>
    <a href="http://legionscripts.com/">
      Website
    </a>
    <span> | </span>
    <a href="https://discord.gg/zg6EPyJ">
      Discord
    </a>
    <span> | </span>
    <a href="https://github.com/legionscripts/legionscripts/blob/master/contributing.md">
      Contributing
    </a>
    <span> | </span>
    <a href="https://github.com/legionscripts/legionscripts/blob/master/customization.md">
      Customization
    </a>
  </h3>
</div>

<div align="center">
  <sub>The Jackpot script that could. Built with ❤︎ by Gergo.
</div>

## Table of Content
- [Information](#information)
- [Getting-Started](#getting-started)
- [Prerequisites](#prerequisites)
- [Deployment](#deployment)
- [Running](#running)
- [Built With](#built-with)

## Information
Hello and thank you for purchasing Legion Jackpot 1.3 BETA. We now have a Provably Fair system!
(note if you have not purchased the script you can find it here <a href="http://legionscripts.com/"> Buy Now</a>)

Legion Scripts is still in BETA so more information should be released shortly about customization and all that.

The main objective now is to test how it works and provide feedback, you can already start a website and customize your script, you have been given a stable release.

Please note this is a BETA release, bugs will be fixed asap.

## Getting-Started

See (Deployment) for notes on how to deploy the project on a live system.

## Prerequisites

What things you need to install the script

```
1GB RAM VPS
Ubuntu 14.04 x64 (recommended)
```

for better support we would recommend the following
```
2GB RAM VPS
Ubuntu 14.04 x64 (recommended)
```
## Deployment

This is the part of the guide will help you deploy the system on a VPS.

```
sudo apt-get update 
sudo apt-get install apache2 
sudo apt-get install mysql-server php5-mysql 
sudo mysql_install_db 
sudo mysql_secure_installation 
apt-get install php5 libapache2-mod-php5 php5-mcrypt 
sudo apt-get install php5-curl 
sudo apt-get install php5-gd 
sudo service apache2 restart 
sudo apt-get install phpmyadmin

cd /var/www/

curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash - 
sudo apt-get install -y nodejs
```

( Be sure to be in the folder /var/www before you install NPM libraries ) 

```
npm install async
npm install sort-by
npm install steam
npm install steam-user
npm install steam-tradeoffer-manager
npm install steam-totp
npm install onceler
npm install request
npm install steamcommunity
npm install node-fs
npm install socket.io-client
npm install log4js
npm install dateformat
npm install mysql
npm install crypto
npm install node-random
npm install mathjs
npm install steam-api
npm install http
npm install socket.io
npm install left-pad
npm install forever -g
```
How to install the web application part of the system.
```
#1.: Upload the Legion.sql file to your PHPMyadmin
#2.: Web: Edit your link.php so it connects properly to your MYSQL database
#3.: Web: Steamauth/SteamConfig.php - > Set up your site's domain, and your bot's API key
#4.: Log in on the site, then navigate to your PHPMyadmin and give yourself a level 3 admin
#5.: Go to your admin panel (you click your picture on the top right, then click "admin") and edit your settings.
#6.: You upload every other bot/server files to your /var/apps folder, you have to create an apps folder.
#7.: Get a steamapi.io key for pricing from steamapi.io, you will need to enter it to your configuration file.
#8.: Set up MYSQL Connection, BOT and SERVER information properly in config/config.js such as: Admin, Owner info, bot information, socket information, sitename, etc.
#9.: Install the required libraries, navigate to your /var/apps folder (cd/var/apps) and install the following libraries (sorry of some of them are listed twice):
```
PLEASE DO NOT USE /var/www/html FOR YOUR BOTS/SERVER FILES!

## Running

Use node first to start your server and / or bot, close the process by pressing CTRL+C once you confirm it works or it returns an error:
```
node legion-bot.js
node legion-server.js
```
Wait a few seconds after trying to launch each to see if everything works properly and it is not returning any errors. If it's returning errors check if you've set up everything correctly, or contact us on Discord.

Once you are sure everything runs smoothly, run both files using forever:
```
forever start legion-bot.js
forever start legion-server.js
```
That way everything will run smoothly without issues, and your site should be up and ready to go.

## Other

Small addition to the installation guide provided: You have to edit your js/script.js, edit the IP / Port to your website's IP (or domain) and the Port you provided in your legion-server.js (2086 by default, it's a port accepted by cloudflare also)

Check out our addons on legionscripts.com/whmcs , more products coming soon, we already have a coinflip available.

If you need help installing your VPS you can purchase an installation addon.

## Built-With

* [Node](https://github.com/nodejs/node/blob/master/README.md) - JavaScript Web Runtime
* [Npm](https://github.com/npm/npm) - Package Manager
* [Php](https://github.com/docker-library/php) - Hypertext Preprocessor
