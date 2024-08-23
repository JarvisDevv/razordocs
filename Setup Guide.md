---
icon: book 
order: 99
---
# Setup Guide
## 1. Prerequisites
*Before installing and running Razor, ensure you have the following:*

- **Node.js v18 LTS:** The bot is built using Node.js, so make sure you have the latest Long-Term Support (LTS) version installed.
- **A Text Editor:** Such as Visual Studio Code or Sublime Text.
- **A Discord Bot Token:** You can create one from the [Discord Developer Portal](https://discord.com/developers/applications).

## 2. Installing Node.js v18 LTS
### Download Node.js:

1. Visit the official Node.js website.
2. Download the [v18 LTS](https://nodejs.org/en/blog/release/v18.18.0) installer for your operating system (Windows, macOS, or Linux).
### Install Node.js:

1. Run the installer and follow the prompts to complete the installation.
2. Make sure to check the option to install npm (Node Package Manager) during the installation process.
### Verify Installation:

1. Open a terminal or command prompt.
2. Type `node -v` and press Enter. This should output the installed Node.js version **(e.g., v18.x.x)**.
Similarly, type `npm -v` to check the npm version.
![](/Public/img/nodejs.png)
## 3. Extracting the Files
### Locate the ZIP File:

- Once the download is complete, locate the downloaded ZIP file on your computer.
### Extract the Files:

- Right-click on the ZIP file and choose "Extract All..." if you are using *Windows*, or select "**Extract Here**" or "**Extract to [Folder Name]**" if you are using **WinRAR** or **7-Zip**.
- Choose a destination folder where you want to extract the files. It’s recommended to extract them to a dedicated folder named razor-bot or something similar.
### Check Extracted Files:

- Open the folder where you extracted the files to ensure all files and directories are present and extracted correctly.

## 4. Installing NPM Packages
### Install Dependencies:
- In the terminal of the source code directory, run the following command to install all necessary npm packages:
```js
npm install
```
OR 
```js
npm install --force 
// In Case If The npm install doesn't work :)
```
- This will read the `package.json` file and install all required dependencies.

## 5. Configuring config.js and .env
### Configuring config.js
#### 1. **Open config.js**:

- Use your preferred text editor to open the `config.js` file located in the bot’s root directory.
#### 2. **Edit Configuration Settings**:

- Fill in the necessary configuration details such as the bot’s prefix, owner ID, and other customizable settings.
- Example:
```js
module.exports = {
  prefix: '!', // Your bot's prefix
  ownerID: 'YOUR_DISCORD_ID', // Your Discord user ID
  // Add other configurations as needed and yeah its example
};
```
## Setting Up .env
#### 1. Rename env File:
- Rename `example.env` to .`env`
#### 2. Add Environment Variables:

- Open the `.env` file in your text editor and add your Discord bot token and other sensitive information.
- Example:
```env
token=YOUR_DISCORD_BOT_TOKEN
mongodb=YOUR_MONGODB_CONNECTION_STRING
```
Replace **YOUR_DISCORD_BOT_TOKEN** with your actual bot token and **YOUR_MONGODB_CONNECTION_STRING** with your MongoDB connection string if the bot uses a database.

## 6. Running Razor
#### Start the Bot:

- In the terminal, run the following command to start the bot:
```js
node index.js
```