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

## 🎮 Comandi Disponibili

#### 🛠️ TOOLS
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| hd | Migliora la qualità di un'immagine | `hd` |
| img | Cerca immagini | `img <termine>` |
| doc | Cerca documenti | `doc <termine>` |
| tiktok | Scarica video da TikTok | `tiktok <link>` |
| instagram | Scarica contenuti da Instagram | `instagram <link>` |
| dado | Lancia un dado | `dado` |
| meteo | Controlla il meteo | `meteo <città>` |
| info | Mostra informazioni generali | `info` |
| proprietario | Informazioni sul proprietario del bot | `proprietario` |
| ping | Verifica la latenza del bot | `ping` |
| lyrics | Cerca testi di canzoni | `lyrics <canzone>` |
| stt | Speech to text | `stt` (con audio) |
| igstalk | Stalk profilo Instagram | `igstalk <username>` |
| toanime | Converti immagine in stile anime | `toanime` (con immagine) |
| toimg | Converti sticker in immagine | `toimg` (con sticker) |
| tomp3 | Converti video in audio | `tomp3` (con video) |
| tovideo | Converti GIF in video | `tovideo` (con GIF) |
| sticker/s | Crea sticker | `sticker` (con immagine) |
| phishy | AI chatbot | `phishy <messaggio>` |
| contautenti | Conta gli utenti nel gruppo | `contautenti` |
| ispeziona | Ispeziona informazioni di un utente | `ispeziona` |
| sito | Informazioni su un sito web | `sito <url>` |
| virus | Scansiona file per virus | `virus` (con file) |
| translate | Traduce testo | `translate <testo>` |
| wiki | Cerca su Wikipedia | `wiki <termine>` |
| gender | Predice il genere da un nome | `gender <nome>` |
| paese | Informazioni su un paese | `paese <nome>` |
| consigliafilm | Consiglia film | `consigliafilm` |
| filtra | Filtra contenuti | `filtra` |

-----
#### 🎭 AZIONI  
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| dance | Fai ballare qualcuno | `dance @utente` |
| sposa | Sposa qualcuno | `sposa @utente` |
| divorzia | Divorzia da qualcuno | `divorzia @utente` |
| bankai | Attacco bankai | `bankai @utente` |
| bonk | Colpisci qualcuno | `bonk @utente` |
| ditalino | Azione provocatoria | `ditalino @utente` |
| sega | Azione provocatoria | `sega @utente` |
| sfida | Sfida qualcuno | `sfida @utente` |
| wwe | Wrestling match | `wwe @utente` |
| abbraccio | Abbraccia qualcuno | `abbraccio @utente` |
| insulta | Insulta qualcuno | `insulta @utente` |
| lite | Litiga con qualcuno | `lite @utente` |
| animeinfo | Informazioni su anime | `animeinfo <nome>` |
| mangainfo | Informazioni su manga | `mangainfo <nome>` |
| misura | Misura attributi | `misura pene/bocce @utente` |
| qrcode | Genera QR code | `qrcode <testo>` |
| sposami | Proposta di matrimonio | `sposami @utente` |
| lega | Lega qualcuno | `lega @utente` |

-----
#### 🏅 TOP
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| top | Classifica generale | `top` |
| topbestemmie | Top bestemmie | `topbestemmie` |
| topdolci | Top dolci | `topdolci` |
| topgay | Top gay | `topgay` |
| topscimmie | Top scimmie | `topscimmie` |
| top5 | Top 5 generale | `top5` |
| settimana | Classifica settimanale | `settimana` |

-----
#### 🎰 GIOCHI
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| blackjack | Gioca a blackjack | `blackjack` |
| slot | Gioca alle slot machine | `slot` |
| poker | Gioca a poker | `poker` |
| gara | Organizza una gara | `gara @utente` |
| math | Gioco matematico | `math` |
| canzone | Indovina la canzone | `canzone` |
| obbligo/verita | Obbligo o verità | `obbligo` o `verita` |
| triss | Gioca a tris | `triss` |
| cfs | Challenge fight system | `cfs` |
| missioni | Sistema missioni | `missioni` |
| missionihelp | Aiuto missioni | `missionihelp` |
| accetta | Accetta missione | `accetta` |
| mymissioni | Le tue missioni | `mymissioni` |
| annulla | Annulla missione | `annulla` |
| verifica | Verifica missione | `verifica` |
| ricaricamissioni | Ricarica missioni | `ricaricamissioni` |

-----
#### 🎉 FUN
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| cr7 | Tributo a Cristiano Ronaldo | `cr7` |
| fototeta | Foto divertenti | `fototeta` |
| ridi | Fai ridere | `ridi @utente` |
| amore | Livello di amore | `amore @utente` |
| guilty | Livello di colpevolezza | `guilty @utente` |
| hornycard | Carta del desiderio | `hornycard @utente` |
| jail | Manda in prigione | `jail @utente` |
| kebab | Ordina kebab | `kebab` |
| odio | Livello di odio | `odio @utente` |
| rispetto | Livello di rispetto | `rispetto @utente` |
| gatto | Immagini di gatti | `gatto` |
| personalita | Analizza personalità | `personalita @utente` |
| emojimix | Mescola emoji | `emojimix 😀+😍` |
| attp/ttp | Testo animato | `attp <testo>` |
| ricetta | Ricette casuali | `ricetta` |
| f1 | Informazioni Formula 1 | `f1` |



### 👑 Admin

#### 🗣️ GRUPPO 
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| add | Aggiungi utente al gruppo | `add <numero>` |
| fixscudi | Ripara problemi del gruppo | `fixscudi` |
| setwelcome/setbye | Imposta messaggio di benvenuto/addio | `setwelcome <messaggio>` |
| set | Impostazioni gruppo | `set <opzione>` |
| aperto/chiuso | Apri/chiudi gruppo | `aperto` o `chiuso` |
| del | Elimina messaggio | `del` (rispondi al messaggio) |
| inattivi | Lista utenti inattivi | `inattivi` |
| kick | Espelli utente | `kick @utente` |
| kicknum | Espelli per numero | `kicknum <numero>` |
| muta/smuta | Silenzia/riattiva utente | `muta @utente` |
| setmuta | Imposta durata silenzio | `setmuta <tempo>` |
| promuovi/p | Promuovi ad admin | `promuovi @utente` |
| retrocedi/r | Rimuovi admin | `retrocedi @utente` |
| simula | Simula azione | `simula <azione>` |
| warn | Avvisa utente | `warn @utente <motivo>` |
| unwarn | Rimuovi avvertimento | `unwarn @utente` o `unwarn 1/2/all` |
| warnlist | Lista avvertimenti | `warnlist` |
| setig | Imposta immagine gruppo | `setig` (con immagine) |
| speedtest | Test velocità connessione | `speedtest` |
| infostato | Informazioni stato gruppo | `infostato` |

----------
#### 👥 TAG FUNZIONI
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| hidetag | Tag nascosto a tutti | `hidetag <messaggio>` |
| tagall | Tagga tutti i membri | `tagall <messaggio>` |
| tagmembri | Tagga solo i membri | `tagmembri <messaggio>` |
| admins | Tagga tutti gli admin | `admins <messaggio>` |
| vaffanculo | Messaggio provocatorio | `vaffanculo` |

---
#### 🎭 FUN COMMANDS 
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| dox | Informazioni fake su utente | `dox @utente` |
| stupra | Azione provocatoria | `stupra @utente` |
| bocchino | Azione provocatoria | `bocchino @utente` |
| bocchina | Azione provocatoria | `bocchina @utente` |


### RPG (role play, economia)

### 📃 STATS
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| profilo | Statistiche nel gioco | `profilo` |
| info | Statistiche generali nel gruppo | `info` |
| livello/level/lvl | Mostra il tuo livello attuale | `livello` |
| levelup/lvlup | Aumenta di livello | `levelup` |
| cura | Curati la vita con le pozioni | `cura` |
| nome/cambianome | Cambia il tuo nome | `nome <nuovo_nome>` |

### 🛒 NEGOZIO
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| shop | Menu del negozio | `shop` |
| compra | Acquista oggetti | `compra <oggetto>` |
| vendi | Vendi oggetti | `vendi <oggetto>` |

### 🍬 CARAMELLE/DOLCI
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| lavoro/sceglilavoro/setjob | Cercati un lavoro | `lavoro` |
| lavora/work | Fai soldi fatturando | `lavora` |
| prega | Meno soldi ma minore cooldown | `prega` |
| ruba | Ruba altri utenti | `ruba @utente` |
| daily | Premio quotidiano | `daily` |
| wallet | Vedi i tuoi soldi | `wallet` |
| deposita | Metti in banca i tuoi dolci | `deposita <numero>` |
| transferisci | Trasferisci oggetti ad altri | `transferisci <numero/oggetto> @utente` |
| tesoro | Ricevi grossi premi | `tesoro` |
| scassa | Scassina cassaforte (serve forcina) | `scassa @utente` |
| missionihelp | Comandi relativi alle missioni | `missionihelp` |

### 🎡 GIOCHI
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| blackjack | Gioca a blackjack | `blackjack` |
| slot | Gioca alle slot machine | `slot` |
| poker | Gioca a poker | `poker` |
| gara | Organizza una gara | `gara @utente` |

### 🐯 ANIMALI/PET
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| bagno | Lava il tuo pet | `bagno` |
| cibo | Dai da mangiare al pet | `cibo` |
| curiosita | Curiosità sul pet | `curiosita` |
| combatti | Fai combattere il pet | `combatti @utente` |
| attacca | Attacca in combattimento | `attacca` |
| difendi | Difenditi in combattimento | `difendi` |
| abilita | Usa abilità speciali | `abilita` |

### 📊 AZIONI E CRYPTO
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| mercato borsa | Mostra dati recenti | `mercato borsa` |
| mercato grafico | Mostra grafico crypto | `mercato grafico <crypto>` |
| mercato compra/vendi | Scambia dolci con crypto | `mercato compra/vendi` |
| azioni | Mostra azioni/crypto possedute | `azioni` |

### 🧙🏻‍♂️ MAGIA
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| reg | Registrati nel mondo magico | `reg` |
| bacchetta | Compra una bacchetta | `bacchetta` |
| borsa | Mostra statistiche e oggetti | `borsa` |
| casata | Il cappello parlante sceglie la casata | `casata` |
| studia | Impara nuove magie | `studia` |
| usa | Lancia un incantesimo | `usa <incantesimo>` |
| dungeon | Entra nel dungeon e combatti | `dungeon` |

-----
### Audio 

| Comando  | Sinonimi |
|----------|----------|
| paguro | cicciogamer |
| grasso | ciccione/a, gross/a, |
| topolino | tiska tuska | mickey |
| topa | bella |
| woman | donna |
| ohno | oh no |
| orcodio | mosconi | gennaro |
| rizz | skibidi, brainrot |
| piedi | piede |
| disco | bober |

### Talk (attivo)

| Comando  | Sinonimi |
|----------|----------|
| come ? | - |
| amo | amore, vita, cucciola |
| basta | - |
| buongiorno | bg |
| buonasera | bs |
| buonanotte | bn |
| bot | robot |
| jurida | . |
| napoli | napoletano |
| vaffanculo | - |













-
#### 🎯 Utility
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| `!weather` | Meteo | `!weather Roma` |
| `!translate` | Traduci testo | `!translate en it Hello` |
| `!qr` | Genera QR code | `!qr Testo` |

-----
#### 🎵 Media
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| `!ytdl` | Download YouTube | `!ytdl [url]` |
| `!sticker` | Crea sticker | Rispondi a immagine |
| `!tts` | Text to speech | `!tts Ciao mondo` |








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
