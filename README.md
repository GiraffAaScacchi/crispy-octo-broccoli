</p> 
 <p align="center"> 
  # 𝐏𝐡𝐢𝐒𝐡𝐲 𝐅𝐜𝐤 𝐔 𝐁𝐨𝐭
 
 </p>

</p> 
 <p align="center"> 

  <img width="400" src="https://i.ibb.co/SDmvw1hZ/Screenshot-2025-06-21-002946.png?color=red&label=Repo%20Size&style=for-the-badge&logo=appveyor"> 
 </p> 

<p align="center">
  <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" />
  <img src="https://img.shields.io/badge/WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" />
  <img src="https://img.shields.io/badge/Social-FF0069?style=for-the-badge&logo=Instagram&logoColor=white" />
</p>


# Indice
- [Descrizione](#Descrizione)
- [Installazione](#Installazione)
- [Funzioni](#Funzioni)
- [Comandi](#Comandi)

## Descrizione

Bot WhatsApp avanzato costruito con [whiskeysockets/baileys](https://github.com/WhiskeySockets/Baileys), una libreria JavaScript per interagire con l'API Web di WhatsApp. Questo bot offre varie opzioni per aiutare gli amministratori e contiene tanti comandi divertenti e intressanti da usare per gli utenti.


## 🎯 Funzionalità Principali
con funzioni si intende vari bottoni on/off che controllano funzioni automatiche del bot. da usare con .attiva o .disabilita... usateli sulle vostre preferenze.

### per il gruppo





| funzione | Descrizione | Uso |
|---------|------|-----|
| detect | questa funzione serve per far funzionare vari comandi come dare admin o rimuovere utenti, lasciatela sempre attiva | ✅ |
| benvenuto | saluta gli utenti quando entrano. i messaggi di  benvenuto, bentornato e addio sono tutti personalizzabili e diversi per ogni gruppo | ✅ |
| modoadmin | se è attivo in quel gruppo solo gli admin possono usare i comandi | ✅ |
| talk | quando è attivo PhiShy risponde agli insulti e interagisce a caso con gli utenti, da usare con cautea 🛑 | ✅ |
| autolevelup | tutti gli utenti salgono di livello appena raggiungono gli exp necessari | ✅ |
| antielimina | manda in privato all'owner i messaggi eliminati in una chat | ✅ |

### restrizioni
| funzione | Descrizione | Uso |
|---------|---------|-----|
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

## 🚀 Installazione 

### 📱 Termux (Android)

Aggiorna i pacchetti
```bash
pkg update && pkg upgrade
```

Installa dipendenze
```bash
pkg install nodejs git python
```

Clona il repository
```bash
git clone https://github.com/[tuo-username]/[nome-repo].git
cd [nome-repo]
``` 
Installa dipendenze npm
```
npm install
```
Avvia il bot
```bash
npm start
```

### 💻 Windows

#### Prerequisiti: Node.js 16+ e Git installati
* scarica e installa Git [`Qui`](https://git-scm.com/downloads)
* scarica e installa NodeJS [`QUi`](https://nodejs.org/en/download)
* scarica e installa FFmpeg [`QUi`](https://ffmpeg.org/download.html) (**Non dimenticare di aggiungere FFmpeg alla variabile d'ambiente PATH.**)
* scarica e installa ImageMagick [`QUi`](https://imagemagick.org/script/download.php)


Clona il repository
```bash
git clone https://github.com/[tuo-username]/[nome-repo].git
cd [nome-repo]
```

Installa dipendenze
```bash
npm install -g ffmpeg imagemagick nodejs
```

Avvia il bot
```bash
npm start
```

🐳 Docker (Opzionale)
Build immagine
```bash
docker build -t whatsapp-bot .
```
Run container
```bash
docker run -d --name wa-bot -v $(pwd)/sessions:/app/sessions whatsapp-bot
```

## ⚙️ Impostazioni

### 1. Configurazione
cerca il file `config.js` e modifica il numero e il nome del proprietario, se sei da telefono usa qualche editor oppure usa 
`pkg install nano` e poi `nano config.js` per usare l'editor su termux, se usi il pc scarica [vs studio](https://code.visualstudio.com/download) ma funziona anche il blocco note:

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
   
2. Dopo il caricamento scrivi 1 o 2 per scegliere come unire il bot con il tuo numero.

  ➪ se hai scelto con codice QR apri WhatsApp, apri ⋮ , poi apri Dispositivi_collegati/Collega un dispositivo, ti si aprirà la fotocamera e       dovrai scanerizzare il codice che ti appare sul terminale.
  
  ➪ se hai scelto con codice a 6 cifre arriva lo stesso a Collega un dispositivo, e poi cliccare in basso sulla scritta "In alternativa, collega con il numero di telefono", inserire nel terminale il numero di telefono e inserire sul telefono il codice che ti viene mostrato nel terminale.

4. Se tutto va bene, il bot si connetterà automaticamente, ti chiederà all'inzio di fare un riavvio, non te lo chiederà più le prossime volte.

## Lista di comandi 

### 👻 Comandi per tutti gli utenti

🛠️ TOOLS
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| hd | Migliora la qualità di un'immagine | `hd` |
| img | Cerca immagini | `img <termine>` |
| doc | leggi la documentazione | `doc <termine>` |
| tiktok | Scarica video da TikTok | `tiktok <link>` |
| instagram | Scarica video da Instagram | `instagram <link>` |
| dado | Lancia un dado | `dado` |
| meteo | Controlla il meteo | `meteo <città>` |
| info | Mostra le tue statistiche generali| `info` |
| proprietario | Informazioni sul proprietario del bot | `proprietario` |
| ping | Verifica la latenza del bot | `ping` |
| lyrics | Cerca testi di canzoni | `lyrics <canzone>` |
| tts | text to Speech | `tts <scrivi qualcosa>`  |
| igstalk | Stalk profilo Instagram | `igstalk <username>` |
| toanime | Converti immagine in stile anime | `toanime` (con immagine) |
| toimg | Converti sticker in immagine | `toimg` (con sticker) |
| tomp3 | Converti video in audio | `tomp3` (con video) |
| tovideo | Converti GIF in video | `tovideo` (con GIF) |
| sticker/s | Crea sticker | `sticker` (con immagine) |
| phishy | AI chatbot | `phishy <messaggio>` |
| contautenti | Conta gli utenti nel database | `contautenti` |
| virus | Scansiona un link  | `virus` (link) |
| translate | Traduce testo, avvolte anche i dialetti | `translate <testo>` |
| wiki | Cerca su Wikipedia | `wiki <termine>` |
| paese | Informazioni su un paese | `paese <nome>` |
| filtra | blocca una parola per 24 ore | `filtra <parola>` |
| animeinfo | Informazioni su anime | `animeinfo <nome>` |
| mangainfo | Informazioni su manga | `mangainfo <nome>` |

-----
🎭 AZIONI  
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| dance | Balla con qualcuno | `dance @utente` |
| sposa | Sposa qualcuno | `sposa @utente` |
| divorzia | Divorzia da qualcuno | `divorzia @utente` |
| bankai | Attacco bankai con Gif| `bankai @utente` |
| bonk | Colpisci qualcuno con il bonki bonko cano | `bonk @utente` |
| ditalino | ditalina una persona | `ditalino @utente` |
| sega | fai una sega a qualcuno | `sega @utente` |
| sfida | comando dedicato a One Piece simile a bankai | `sfida @utente` |
| wwe | attacco con mossa da Wrestling | `wwe @utente` |
| abbraccio | Abbraccia qualcuno | `abbraccio @utente` |
| insulta | Insulta qualcuno | `insulta @utente` |
| lite | fai litigare due persone a caso | `lite @utente` |
| misura | Misura attributi | `misura pene/bocce @utente` |
| qrcode | Genera QR code | `qrcode <testo>` |
| sposami | TI propone qualcuno con cui poterti sposare | `sposami @utente` |
| lega | Lega qualcuno | `lega @utente` |

-----
🏅 TOP
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| top | Classifica dei messaggi | `top` |
| topbestemmie | Classifica bestemmie | `bestemmie` |
| topdolci | Classifica di chi ha più dolci | `topdolci` |
| topgay | Top gay | `topgay` |
| topscimmie | Top scimmie | `topscimmie` |
| top5 | Top cincos videos espagnol | `top5` |
| settimana | Classifica settimanale | `settimana` |

-----
🎰 GIOCHI
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| blackjack | Gioca a blackjack contro il bot| `blackjack` |
| slot | Gioca alle slot machine | `slot` |
| poker | Gioca a poker (contiene ancora molti bug) | `poker` |
| gara | fai una gara di moto o macchina contro qualcuno, ma solo se ne hai comprata una | `gara @utente` |
| math | Giochi di matematica | `math` |
| canzone | Indovina la canzone (contine bug) | `canzone` |
| obbligo/verita | Obbligo o verità | `obbligo` o `verita` |
| triss | Gioca a tris | `triss` |
| cfs | carta forbici sasso contro il bot | `cfs` |

-------
MISSIONI 📢
| missionihelp | Comandi relativi alle missioni | `missionihelp` |
|---------|----------|-------|
| missioni | vedi le missioni disponibili | `missioni` |
| accetta | Accetta missione | `accetta` |
| mymissioni | Le tue missioni | `mymissioni` |
| annulla | Annulla missione | `annulla` |
| verifica | Verifica missione (admin) | `verifica` |
| ricaricamissioni | Ricarica missioni (admin)| `ricaricamissioni` |

-----
🎉 FUN
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| cr7 | Tributo a Cristiano Ronaldo | `cr7` |
| fototeta | no spoiler.. | `fototeta` |
| ridi | ridi di qualcuno | `ridi @utente` |
| amore | Livello di amore | `amore @utente` |
| guilty | img di pentito | `guilty @utente` |
| hornycard | img di un pervertito | `hornycard @utente` |
| jail | img di un carcerato | `jail @utente` |
| kebab | Ordina kebab | `kebab` |
| odio | Livello di odio | `odio @utente` |
| rispetto | img di qualcuno con rispetto | `rispetto @utente` |
| gatto | Immagini di gatti casuali | `gatto` |
| personalita | Analizza personalità | `personalita @utente` |
| emojimix | Mescola emoji | `emojimix 😀+😍` |
| attp/ttp | Testo animato con sticker | `attp <testo>` |
| ricetta | Ricette casuali | `ricetta` |
| f1 | comando dedicato a giulia | `f1` |

------
### 👑 Comandi per Admin

🗣️ GRUPPO 
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| add | Aggiungi utente al gruppo | `add <numero>` |
| fixscudi | Ripara il bug dei scudi | `fixscudi` |
| setwelcome/setbye/setbentornato | Imposta messaggio di benvenuto, addio e bentornato | `setwelcome <messaggio>` |
| set | Impostazioni gruppo | `set <opzione>` |
| aperto/chiuso | Apri/chiudi gruppo | `aperto` o `chiuso` |
| del | Elimina messaggio | `del` (rispondi al messaggio) |
| inattivi | Lista utenti inattivi | `inattivi` |
| kick | Espelli utente | `kick @utente` |
| ban | rimuovi l'utente da tutti i gurppi in cui phishy è admin (anche le bacheche) | `ban @utente` o `ban +39 xxx xxx xxxx` |
| kicknum | Espelli per prefisso | `kicknum <numero>` |
| muta/smuta | Silenzia/riattiva utente | `muta @utente` |
| setmuta | Imposta durata silenzio | `setmuta <tempo>` |
| promuovi/p | Promuovi ad admin | `promuovi @utente` |
| retrocedi/r | Rimuovi admin | `retrocedi @utente` |
| simula | Simula azione | `simula <azione>` |
| warn | aggiungi un avvertimento all'utente | `warn @utente <motivo>` |
| unwarn | Rimuovi avvertimento | `unwarn @utente` o `unwarn 1/2/all` |
| warnlist | Lista avvertimenti | `warnlist @utente` o `+39 xxx xxx xxxx` |
| warngroup | Lista avvertimenti | `warngroup` |
| setig | Imposta link di instagram nelle info | `setig @nome_utente`  |
| speedtest | Test velocità connessione | `speedtest` |
| infostato | Informazioni stato gruppo | `infostato` |

----------
👥 TAG FUNZIONI
| Comando | Descrizione | Uso |
|---------|------|-----|
| hidetag | Tag nascosto a tutti | `hidetag <messaggio>` |
| tagall | Tagga tutti i membri | `tagall <messaggio>` |
| tagmembri | Tagga solo i membri normali | `tagmembri <messaggio>` |
| admins | Tagga tutti gli admin | `admins <messaggio>` |
| vaffanculo | insulta tutto il gruppo | `vaffanculo` |

------
🎭 FUN COMMANDS 
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| dox | Informazioni fake su utente (forse) | `dox @utente` |
| stupra | Azione provocatoria | `stupra @utente` |
| bocchino | Azione provocatoria | `bocchino @utente` |









-----
### RPG (role play, economia)

📃 STATS
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| profilo | Statistiche nel gioco | `profilo` |
| info | Statistiche generali nel gruppo | `info` |
| livello/level/lvl | Mostra il tuo livello attuale | `livello` |
| levelup/lvlup | Aumenta di livello | `levelup` |
| cura | Curati la vita con le pozioni | `cura minore/maggiore/definitiva` |
| nome/cambianome | Cambia il tuo nome nel database, utile quando vedi il numero di cell invece del nick | `nome <nuovo_nome>` |

-----
🛒 NEGOZIO
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| shop | Menu del negozio | `shop` |
| compra | Acquista oggetti | `compra <oggetto>` |
| vendi | Vendi oggetti | `vendi <oggetto>` |

-----
🍬 CARAMELLE/DOLCI
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| sceglilavoro/setjob | Cercati un lavoro | `sceglilavoro` |
| lavora/work | Fai soldi fatturando | `lavora` |
| prega | Trova meno soldi ma minore cooldown | `prega` |
| ruba | Ruba ad altri utenti | `ruba @utente` |
| daily | Premio quotidiano | `daily` |
| wallet | Vedi i tuoi soldi | `wallet` |
| deposita | Metti in banca i tuoi dolci | `deposita <numero>` |
| transferisci | Trasferisci oggetti ad altri | `transferisci <numero/oggetto> @utente` |
| tesoro | Ricevi grossi premi dopo il livello 30| `tesoro` |
| scassa | Scassina cassaforte (serve forcina) | `scassa @utente` |
| missionihelp | Comandi relativi alle missioni | `missionihelp` |

-----
🐯 ANIMALI/PET
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| bagno | Lava il tuo pet | `bagno` |
| cibo | Dai da mangiare al pet | `cibo` |
| curiosita | Curiosità sul pet | `curiosita` |
| ✜ combatti | Fai combattere il pet | `combatti @utente` |
| ✜ attacca | Attacca in combattimento | `attacca` |
| ✜ difendi | Difenditi in combattimento | `difendi` |
| ✜ speciale | Usa abilità speciali | `speciale` |

-----
📊 AZIONI E CRYPTO
| Comando | Descrizione | Uso |
|---------|-------------|-----|
| mercato borsa | Mostra dati recenti | `mercato borsa` |
| mercato grafico | Mostra grafico crypto | `mercato grafico <crypto>` |
| mercato compra/vendi | Scambia dolci con crypto | `mercato compra/vendi` |
| azioni | Mostra azioni/crypto possedute | `azioni` |

🧙🏻‍♂️ MAGIA
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

------
### Talk (se è attivo)

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




## Problemi Comuni

#### Bot non si connette
```bash
### Cancella sessione
rm -rf sessions/

### Riavvia bot
npm start
```

#### Errori di memoria
```bash
### Aumenta limite memoria Node.js
node --max-old-space-size=4096 index.js
```

#### Problemi dipendenze
```bash
### Reinstalla dipendenze
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


## 🤝 Contribuire

### Come Contribuire
1. Fork il repository
2. Crea branch feature (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push branch (`git push origin feature/AmazingFeature`)
5. Apri Pull Request


## ⭐ Supporta il Progetto

Se questo bot ti è stato utile, considera di:
- ⭐ Mettere una stella al repository
- 🐛 Segnalare bug o suggerimenti
- 💝 Fare una donazione

## 📊 Statistiche

![GitHub stars](https://img.shields.io/github/stars/tuo-username/nome-repo?style=social)
![GitHub forks](https://img.shields.io/github/forks/tuo-username/nome-repo?style=social)
![GitHub issues](https://img.shields.io/github/issues/tuo-username/nome-repo)
![GitHub license](https://img.shields.io/github/license/tuo-username/nome-repo)

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/easterbones">easter</a>
</p>
