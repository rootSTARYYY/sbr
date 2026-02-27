# 🌌 SBR | Advanced SkyBlock Management

**SBR** is a professional-grade Discord bot built to manage high-traffic Hypixel SkyBlock service servers. From automated carrier applications to dynamic rosters and carry ticket management, SBR handles the heavy lifting of server administration.

---

## 🛠️ Configuration Guide
>  **Caution**: Please don't delete any of the files present in the folder ( might crash the bot ).
To get the bot running, you need to configure two main files.

### 1. `config.js`
This is the heart of the bot. You must fill in the strings between the quotes:

* **MONGODB_URI**: Your MongoDB connection string.
* **BOT_TOKEN**: Your bot token from the Discord Developer Portal.
* **CLIENT_ID**: Your bot's application ID.
* **CATEGORY_IDs**: These define where tickets will be opened.
* **CHANNEL_IDs**: Where the bot will post embeds for carries, applications, and rosters.

### 2. `roles.json`
This file manages your staff permissions and the carrier progression system:

* **Staff**: Define who can manage the bot (`admin` and `mod`).
* **carrierRole**: The main role required to claim tickets.
* **Milestones**: Enter the Role IDs for each carry bracket (e.g., `51-100`, `101-150`). The bot uses these to automatically rank up your carriers.

---

## 🚀 Main Features

### 📋 Carrier Roster System
The bot maintains a live roster in your designated channel. It tracks:
* **Carrier Status**: Online/Offline tracking.
* **Carry Count**: Automatically updates after every "Finished Carry."
* **Feedback**: Displays a rating out of 10 based on customer reviews.

### ⚔️ Carry Ticket System
SBR features a high-end UI for Floor 6, Floor 7, and Master Mode carries.
* **Smart Pricing**: Preset prices for Completion (Comp), S, and S+ runs.
* **Claim System**: Carriers can claim tickets with a single button click.
* **Anti-Scam**: Built-in warnings for payment increments and profile rules.

### 📝 Automated Applications
Users can apply for carrier positions through an interactive button.
* Applications are sent to a private staff channel.
* Staff can Accept/Reject with custom feedback.

---

## 📁 File Structure Overview

| File | Description |
| :--- | :--- |
| `config.js` | Main bot settings and Channel/Category IDs. |
| `roles.json` | Role IDs for staff and carrier milestones. |
| `*.txt files` | Used by the bot to "remember" the ID of posted messages so it can update them later. |

---

## 💻 Installation

1.  **Install Dependencies**:
    ```bash
    npm install
    ```
2.  **Setup Environment**: Fill out `config.js` and `roles.json`.
3.  **Launch**:
    ```bash
    npm start   
    ```
3.  **Commands**:
    ```bash
    npm deploy
    ```
---

> **Developer Note**: Ensure your bot has the `Server Members` and `Message Content` intents enabled in the Discord Developer Portal, or the roster and commands will not function correctly. 


**Powered by SBR Development.**
