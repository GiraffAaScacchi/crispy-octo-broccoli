# 🤖 [Nome del tuo Bot] - WhatsApp Bot

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" />
  <img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" />
  <img src="https://img.shields.io/badge/IG-FF0069?style=for-the-badge&logo=whatsapp&logoColor=white" />
</p>

<p align="center">
  <img src="./assets/preview.gif" alt="Bot Preview" width="600"/>
</p>

## 📝 Descrizione

Bot WhatsApp avanzato costruito con [whiskeysockets/baileys](https://github.com/WhiskeySockets/Baileys), una libreria JavaScript per interagire con l'API Web di WhatsApp. Questo bot offre [descrivi le funzionalità principali del tuo bot].

## ✨ Caratteristiche

### 🎯 Funzionalità Principali
- [ ] **Comandi Admin**: Gestione gruppi, kick/promote utenti
- [ ] **AI Integration**: ChatGPT, Gemini, o altre AI
- [ ] **Media Processing**: Download YouTube, conversione formati
- [ ] **Utility**: Traduttore, weather, news
- [ ] **Games**: Quiz, indovinelli, giochi di gruppo
- [ ] **Moderation**: Anti-spam, anti-link, filtri
- [ ] **Database**: Salvataggio dati utenti/gruppi
- [ ] **Multi-language**: Supporto lingue multiple

### 🛠️ Caratteristiche Tecniche
- [x] **Auto Reconnect**: Riconnessione automatica
- [x] **Session Management**: Gestione sessioni persistenti
- [x] **Error Handling**: Gestione errori robusta
- [x] **Rate Limiting**: Controllo velocità messaggi
- [x] **Plugin System**: Sistema plugin modulare
- [x] **Config System**: Configurazione tramite JSON/ENV

## 🚀 Installazione Rapida

### 📱 Termux (Android)
```bash
# Aggiorna i pacchetti
pkg update && pkg upgrade

# Installa dipendenze
pkg install nodejs git python

# Clona il repository
git clone https://github.com/[tuo-username]/[nome-repo].git
cd [nome-repo]

# Installa dipendenze npm
npm install

# Avvia il bot
npm start
```

### 💻 Windows
```bash
# Prerequisiti: Node.js 16+ e Git installati

# Clona il repository
git clone https://github.com/[tuo-username]/[nome-repo].git
cd [nome-repo]

# Installa dipendenze
npm install

# Avvia il bot
npm start
```

### 🐳 Docker (Opzionale)
```bash
# Build immagine
docker build -t whatsapp-bot .

# Run container
docker run -d --name wa-bot -v $(pwd)/sessions:/app/sessions whatsapp-bot
```

## ⚙️ Configurazione

### 1. File di Configurazione
Crea un file `config.json` nella directory principale:

```json
{
  "botName": "Il Mio Bot",
  "prefix": "!",
  "ownerNumber": "39xxxxxxxxxx",
  "timezone": "Europe/Rome",
  "database": {
    "type": "json",
    "path": "./database/db.json"
  },
  "features": {
    "autoRead": true,
    "autoReact": false,
    "welcomeMessage": true,
    "antiSpam": true
  }
}
```

### 2. Variabili d'Ambiente
Crea un file `.env`:

```env
# API Keys (opzionali)
OPENAI_API_KEY=your_openai_key
GOOGLE_API_KEY=your_google_key
WEATHER_API_KEY=your_weather_key

# Database (se usi MongoDB)
MONGO_URI=mongodb://localhost:27017/whatsappbot

# Altri servizi
WEBHOOK_URL=https://your-webhook.com
```

### 3. Prima Configurazione
```bash
# Copia il file di esempio
cp config.example.json config.json

# Modifica con i tuoi dati
nano config.json

# Avvia per la prima volta
npm run setup
```

## 📱 Come Usare

### Connessione
1. Avvia il bot con `npm start`
2. Scansiona il QR code con WhatsApp
3. Il bot si connetterà automaticamente

### Comandi Base
```
!help - Mostra tutti i comandi
!ping - Testa la connessione
!info - Informazioni sul bot
!menu - Menu principale
```

### Comandi Admin
```
!kick @user - Rimuovi utente dal gruppo
!promote @user - Promuovi a admin
!demote @user - Rimuovi da admin
!group open/close - Apri/chiudi gruppo
```

## 🔧 Personalizzazione

### Aggiungere Nuovi Comandi
```javascript
// commands/mycommand.js
module.exports = {
    name: 'mycommand',
    description: 'Il mio comando personalizzato',
    execute: async (sock, msg, args) => {
        // La tua logica qui
    }
}
```

### Modificare le Risposte
Edita il file `responses.json`:
```json
{
    "welcome": "Benvenuto nel gruppo!",
    "goodbye": "Addio!",
    "error": "Si è verificato un errore"
}
```

### Plugin System
```javascript
// plugins/myplugin.js
module.exports = {
    name: 'myplugin',
    load: () => {
        console.log('Plugin caricato!');
    }
}
```

## 📊 Database

### Supporto Database
- [x] **JSON** (default)
- [x] **MongoDB**
- [x] **MySQL**
- [x] **PostgreSQL**
- [x] **SQLite**

### Schema Dati
```javascript
// Utenti
{
    id: "39xxxxxxxxxx",
    name: "Nome Utente",
    isAdmin: false,
    joinDate: "2024-01-01",
    messageCount: 150
}

// Gruppi
{
    id: "gruppo-id",
    name: "Nome Gruppo",
    settings: {
        welcome: true,
        antiSpam: false
    }
}
```

## 🎮 Comandi Disponibili

### 📋 Generali
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| `!help` | Lista comandi | `!help [categoria]` |
| `!ping` | Test latenza | `!ping` |
| `!uptime` | Tempo online | `!uptime` |

### 👑 Admin
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| `!kick` | Rimuovi utente | `!kick @user` |
| `!ban` | Banna utente | `!ban @user` |
| `!promote` | Promuovi admin | `!promote @user` |

### 🎯 Utility
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| `!weather` | Meteo | `!weather Roma` |
| `!translate` | Traduci testo | `!translate en it Hello` |
| `!qr` | Genera QR code | `!qr Testo` |

### 🎵 Media
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| `!ytdl` | Download YouTube | `!ytdl [url]` |
| `!sticker` | Crea sticker | Rispondi a immagine |
| `!tts` | Text to speech | `!tts Ciao mondo` |

## 🔒 Sicurezza

### Rate Limiting
```javascript
// Limite messaggi per utente
const rateLimit = {
    windowMs: 60000, // 1 minuto
    max: 10 // max 10 messaggi
}
```

### Anti-Spam
- Blocco automatico messaggi ripetuti
- Blacklist parole/link
- Timeout temporanei

### Permessi
```javascript
// Livelli permessi
const PERMISSIONS = {
    USER: 0,
    VIP: 1,
    ADMIN: 2,
    OWNER: 3
}
```

## 📈 Monitoring

### Logs
```bash
# Visualizza logs
tail -f logs/bot.log

# Logs per categoria
npm run logs:error
npm run logs:warn
```

### Statistiche
- Messaggi processati
- Comandi più usati
- Utenti attivi
- Uptime bot

## 🐛 Troubleshooting

### Problemi Comuni

#### Bot non si connette
```bash
# Cancella sessione
rm -rf sessions/

# Riavvia bot
npm start
```

#### Errori di memoria
```bash
# Aumenta limite memoria Node.js
node --max-old-space-size=4096 index.js
```

#### Problemi dipendenze
```bash
# Reinstalla dipendenze
rm -rf node_modules package-lock.json
npm install
```

### Debug Mode
```bash
# Avvia con debug
DEBUG=* npm start

# Solo errori Baileys
DEBUG=baileys* npm start
```

## 📦 Dipendenze

### Principali
```json
{
    "@whiskeysockets/baileys": "^6.x.x",
    "qrcode-terminal": "^0.12.0",
    "pino": "^8.x.x",
    "moment": "^2.x.x"
}
```

### Opzionali
```json
{
    "openai": "^4.x.x",
    "mongoose": "^7.x.x",
    "ytdl-core": "^4.x.x",
    "axios": "^1.x.x"
}
```

## 🚀 Deployment

### VPS/Server
```bash
# Con PM2
npm install -g pm2
pm2 start ecosystem.config.js
pm2 save
pm2 startup
```

### Heroku
```bash
# Login Heroku
heroku login

# Crea app
heroku create nome-bot

# Deploy
git push heroku main
```

### Railway/Render
1. Collega repository GitHub
2. Configura variabili ambiente
3. Deploy automatico

## 🤝 Contribuire

### Come Contribuire
1. Fork il repository
2. Crea branch feature (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push branch (`git push origin feature/AmazingFeature`)
5. Apri Pull Request

### Coding Standards
- Usa ESLint/Prettier
- Commenti in italiano/inglese
- Test per nuove funzionalità
- Documentazione aggiornata

## 📄 License

Distribuito sotto licenza [MIT/GPL-3.0]. Vedi `LICENSE` per maggiori informazioni.

## 👨‍💻 Autore

**[Il Tuo Nome]**
- GitHub: [@tuo-username](https://github.com/tuo-username)
- Telegram: [@tuo-telegram](https://t.me/tuo-telegram)
- WhatsApp: [+39xxxxxxxxxx](https://wa.me/39xxxxxxxxxx)

## 🙏 Ringraziamenti

- [whiskeysockets/baileys](https://github.com/WhiskeySockets/Baileys) - Libreria principale
- [adiwajshing](https://github.com/adiwajshing) - Creatore originale
- Community WhatsApp Bot per supporto e feedback

## ⭐ Supporta il Progetto

Se questo bot ti è stato utile, considera di:
- ⭐ Mettere una stella al repository
- 🐛 Segnalare bug o suggerimenti
- 💝 Fare una donazione

[![PayPal](https://img.shields.io/badge/PayPal-00457C?style=for-the-badge&logo=paypal&logoColor=white)](https://paypal.me/tuo-paypal)
[![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/tuo-kofi)

## 📊 Statistiche

![GitHub stars](https://img.shields.io/github/stars/tuo-username/nome-repo?style=social)
![GitHub forks](https://img.shields.io/github/forks/tuo-username/nome-repo?style=social)
![GitHub issues](https://img.shields.io/github/issues/tuo-username/nome-repo)
![GitHub license](https://img.shields.io/github/license/tuo-username/nome-repo)

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/tuo-username">Il Tuo Nome</a>
</p>
