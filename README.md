# esp32_BotTelegram_GPIO
control pin gpio with bot telegram using ESP32

# Lista componenti

* ESP32-WROVER
* Breadboard
* LED
* resistor 220 ohm
* 2x jumper
* GPIO extension board (falcolatitivo)

![alt text](https://i0.wp.com/www.moreware.org/wp/wp-content/uploads/2022/08/ltc.png?w=616&ssl=1)

# Collegamenti

![alt text](https://i0.wp.com/www.moreware.org/wp/wp-content/uploads/2022/08/ltc-1.png?w=600&ssl=1)

# Creare bot telegram

Il primo passo consiste nell’aprire l’applicazione telegram. Una volta aperta cerchiamo “BotFather” tramite la funzione cerca cliccando sull’apposita lente di ingrandimento.

“BotFather” è un bot che permette di creare altri bot.

Avviamo il bot scrivendo “/start“, poi premiamo invio.

![alt text](https://i0.wp.com/www.moreware.org/wp/wp-content/uploads/2020/12/bothfather1.png?w=623&ssl=1)

Per creare un nuovo bot digitiamo “/newbot”.

BotFather ci chiederà di assegnare un nome al nostro nuovo Bot, basta digitare un qualsiasi nome e poi premere Invio.

Dobbiamo anche inserire un username che lo renderà riconoscibile pubblicamente. Username deve terminare in “Bot” o ” _bot”.

In seguito alla assegnazione del nome e dell’username BotFather ci comunicherà informazioni importanti in seguito per compilare il codice per il funzionamento della camera e dell’invio dati. ATTENZIONE: QUESTE INFOMAZIONI LE DOVREMMO TENERE SOLO PER NOI. La prima parte riguarda il percorso per trovare il nostro bot. La seconda è la API che sarà utilizzato nel nostro codice.

![alt text](https://i0.wp.com/www.moreware.org/wp/wp-content/uploads/2020/12/botfather2.png?w=618&ssl=1)

# Ottenere chat id

Per recuperare il chat_id bisogna andare al link https://api.telegram.org/bot<TOKEN>/getUpdates, dove al posto di <TOKEN> dovete inserire il TOKEN di accesso alle API http del bot.

A questo punto mandate un messaggio nella chat ed aggiornate la pagina del link. In questa pagina vedrete popolarsi un file JSON in cui vi viene mostrato il CHAT_ID nella chiave “chat” e nel campo “id” (come nello screenshot sottostante):
  
![alt text](https://i0.wp.com/www.moreware.org/wp/wp-content/uploads/2021/10/Screenshot_2020-05-06-https-api-telegram-org-1024x48-1.png?resize=768%2C36&ssl=1
  
In alternativa inserisci il token nell'apposito form per ottenere il chat id del tuo bot, il tutto è abbastanza autoesplicativo
https://codesandbox.io/s/get-telegram-chat-id-q3qkk
  
  # Codice
Se questo è il tuo primo articolo ti invito di leggere prima questo per l’installazione dei driver della scheda. Ecco qui un piccolo riepilogo prima di compilare e caricare il codice.

![alt text](https://i0.wp.com/www.moreware.org/wp/wp-content/uploads/2022/08/ltc-2.png?w=599&ssl=1)
![alt text](https://i0.wp.com/www.moreware.org/wp/wp-content/uploads/2022/08/ltc-3.png?w=557&ssl=1)
  
Dobbiamo installare la libreria dht.h, dobbiamo andare su Sketch->Include library-> Manage libraries e cercare nell’apposito menù la libreria dht.h.

![alt text](https://i0.wp.com/www.moreware.org/wp/wp-content/uploads/2023/01/adafruit_dht_library.png?w=750&ssl=1)

Dobbiamo installare la libreria UniversalTelegramBot.h, dobbiamo andare su Sketch->Include library-> Manage libraries e cercare nell’apposito menù la libreria UniversalTelegramBot.h.

![alt text](https://i0.wp.com/www.moreware.org/wp/wp-content/uploads/2022/08/FRSHLA9JQQYK3OF.png?resize=768%2C437&ssl=1)

# Codice 
 Link Codice https://github.com/SimoneMoreWare/esp32_BotTelegram_GPIO/blob/main/LedBot.ino
  
# Conclusione
  carica il codice
  ![alt text](https://i0.wp.com/www.moreware.org/wp/wp-content/uploads/2022/09/ESP32-ESP8266-NodeMCU-Telegram-Control-Outputs-Overview.png?w=856&ssl=1)
