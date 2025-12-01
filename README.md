# Chatroom# MQTT Chat

MQTT Chat on reaaliaikainen chat-sovellus, joka käyttää **MQTT-protokollaa**, **MySQL-tietokantaa** ja **Flask REST API:a**. Sovellus toimii LEMP-stackilla (Linux, Nginx, MySQL, Python) ja voidaan käynnistää Docker-kontin avulla.


---

## Ominaisuudet

- Reaaliaikainen chat WebSocketin kautta selaimessa
- MQTT broker Docker-kontissa (Eclipse Mosquitto)
- Viestien tallennus MySQL-tietokantaan
- REST API vanhojen viestien hakemiseen
- Scrollattava chat-ikkuna, vakio korkeus
- Automaattinen nick-tallennus selaimen localStorageen
- Systemd-palvelut MQTT Loggerille ja Flask API:lle

---

## Tiedostorakenne

~/mqtt-chat/
├── docker-compose.yml # Mosquitto Docker Compose
├── mqtt_logger.py # MQTT -> MySQL logger
├── api.py # Flask REST API
├── README.md # Tämä tiedosto
└── mosquitto/
├── config/
│ └── mosquitto.conf
├── data/
└── log/
