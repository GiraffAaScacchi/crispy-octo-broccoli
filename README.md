# Indice
- [Descrizione](#Descrizione)
- [Installazione](#Installazione)
- [Funzioni](#Funzioni)
- [Comandi](#Comandi)

</p> 
 <p align="center"> 
  <img width="400" src="https://i.ibb.co/SDmvw1hZ/Screenshot-2025-06-21-002946.png?color=red&label=Repo%20Size&style=for-the-badge&logo=appveyor"> 
 </p> 

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" />
  <img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" />
  <img src="https://img.shields.io/badge/Social-FF0069?style=for-the-badge&logo=Instagram&logoColor=white" />
</p>

## Descrizione

Bot WhatsApp avanzato costruito con [whiskeysockets/baileys](https://github.com/WhiskeySockets/Baileys), una libreria JavaScript per interagire con l'API Web di WhatsApp. Questo bot offre varie opzioni per aiutare gli amministratori e contiene tanti comandi divertenti e intressanti da usare per gli utenti.


## 🎯 Funzionalità Principali
con funzioni si intende vari bottoni on/off che controllano funzioni automatiche del bot. da usare con .attiva o .disabilita... usateli sulle vostre preferenze.

### per il gruppo





| funzione | Descrizione | Uso |
|---------|-------------|-----|
| detect | questa funzione serve per far funzionare vari comandi come dare admin o rimuovere utenti, lasciatela sempre attiva | ✅ |
| benvenuto | saluta gli utenti quando entrano. i messaggi di  benvenuto, bentornato e addio sono tutti personalizzabili e diversi per ogni gruppo | ✅ |
| modoadmin | se è attivo in quel gruppo solo gli admin possono usare i comandi | ✅ |
| talk | quando è attivo PhiShy risponde agli insulti e interagisce a caso con gli utenti, da usare con cautea 🛑 | ✅ |
| autolevelup | tutti gli utenti salgono di livello appena raggiungono gli exp necessari | ✅ |
| antielimina | manda in privato all'owner i messaggi eliminati in una chat | ✅ |

### restrizioni
| funzione | Descrizione | Uso |
|---------|-------------|-----|
| antiarab | kicka fuori chi scrive da numeri stranieri | ✅ |
| antiporno | ancora in fase di sviluppo, non lascia che utenti mandino materiale nsfw | ❌ |
| antitrava | riconosce messaggi troppo lunghi e li elimina | ✅ |
| antilink | non permette link di altri gruppi WhatsApp | ✅ |
| antivoip | rifiuta automaticamente le richieste ai gruppi di tutti i voip | ✅ |
| bottoni | deprecati anni fa, non sono importarti per le funzioni del bot | ❌ |
| antispam | avverte di ban chi scrive troppi messaggi in poco tempo, dopodiché verrà bannato | ✅ |
| anticall | il bot blocca chi lo chiama | ✅ |
| antiprivato | il bot blocca la persona che gli scrive in prvivato | ✅ |

### altro

| sologruppo | i comandi non funzionano in privato | ✅ |
|---------|-------------|-----|
| soloprivato | i comandi non funzionano nei gruppi | ✅ |



### 🛠️ Caratteristiche Tecniche
- [x] **Auto Reconnect**: Riconnessione automatica
- [x] **Session Management**: Gestione sessioni persistenti
- [x] **Error Handling**: Gestione errori robusta
- [x] **Rate Limiting**: Controllo velocità messaggi
- [x] **Plugin System**: Sistema plugin modulare
- [x] **Config System**: Configurazione tramite JSON/ENV

# 🚀 Installazione 

### 📱 Termux (Android)

#### Aggiorna i pacchetti
```bash
pkg update && pkg upgrade
```

#### Installa dipendenze
```bash
pkg install nodejs git python
```

#### Clona il repository
```bash
git clone https://github.com/[tuo-username]/[nome-repo].git
cd [nome-repo]
``` 

#### Installa dipendenze npm
```
npm install
```

#### Avvia il bot
```bash
npm start
```

### 💻 Windows

#### Prerequisiti: Node.js 16+ e Git installati

#### Clona il repository
```bash
git clone https://github.com/[tuo-username]/[nome-repo].git
cd [nome-repo]
```

#### Installa dipendenze
```bash
npm install -g ffmpeg imagemagick nodejs
```

#### Avvia il bot
```bash
npm start
```

#### 🐳 Docker (Opzionale)
#### Build immagine
```bash
docker build -t whatsapp-bot .
```
#### Run container
```bash
docker run -d --name wa-bot -v $(pwd)/sessions:/app/sessions whatsapp-bot
```

## ⚙️ Configurazione

### 1. Prime configurazioni
cerca il file `config.js` e modifica il numero e il nome del proprietario, se sei da telefono usa qualche editor oppure usa 
`pkg install nano` e poi `nano config.js` per usare l'editor su termux:

```node js
global.owner = [

  ['390001113333@s.whatsapp.net', '𓊈ҽαʂƚҽɾ𓊉𓆇𓃹', true],
  ['392225557777@s.whatsapp.net', 'puoi aggiungere altri owner' ]

]
```

puoi anche modificare altre cose come il nome del bot o l'autore dei pacchetti di stickers:
```node js
global.packname = ``
global.author = '{\n "bot": {\n   "name": "PᏂ𝚒𝑠𝐡ⲩ ᶠᶸᶜᵏᵧₒᵤ!",\n     "author": "easter",\n   "status_bot": "active"\n }\n}'
global.wait = '🐢 *PᏂ𝚒𝑠𝐡ⲩ ᶠᶸᶜᵏᵧₒᵤ!*'
global.botname = 'PᏂ𝚒𝑠𝐡ⲩ ᶠᶸᶜᵏᵧₒᵤ!'
global.textbot = `buongiorno`
global.listo = '*🍭 Aqui tiene*'
global.namechannel = '【 PᏂ𝚒𝑠𝐡ⲩ ᶠᶸᶜᵏᵧₒᵤ! 】'
```

### 2. Variabili d'Ambiente
Crea un file di nome `.env` se vuoi usare le tue API fuori dagli script:

```env
# API Keys (opzionali)
OPENAI_API_KEY=your_openai_key
GOOGLE_API_KEY=your_google_key

```


## Installazione

### Connessione
1. Avvia il bot con `npm start` oppure `node index.js` oppure `node .`
2. Dopo il caricamento scrivi 1 o 2 per scegliere come unire il bot con il tuo numero. \n
   ➪ se hai scelto con codice QR apri WhatsApp, apri ⋮ , poi apri Dispositivi_collegati/Collega un dispositivo, ti si aprirà la fotocamera e       dovrai scanerizzare il codice che ti appare sul terminale.\n
   ➪ se hai scelto con codice a 6 cifre arriva lo stesso a Collega un dispositivo, e poi cliccare in basso sulla scritta "In alternativa, collega con il numero di telefono", inserire nel terminale il numero di telefono e inserire sul telefono il codice che ti viene mostrato nel terminale.
3. Se tutto va bene, il bot si connetterà automaticamente, ti chiederà all'inzio di fare un riavvio, non te lo chiederà più le prossime volte.

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
