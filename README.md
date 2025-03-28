# TP_controleur_AmalrajJCV_MarieMM

## Fait par
- Amalraj John Charles Varatharajan
- Mariam Mougammadou

## Démarrage

On commence par créer le projet, initialiser les périphériques par défaut. On fait un test avec la LED LD2 de la carte NUCLEO, ainsi qu'avec un printf pour voir que tout fonctionne correctement.

## GPIO Expander 

### Configuration

La référence du GPIO expander est la puce MCP23S17. Il y a 16 leds connectés sur la puce. 
Nous allons utiliser le SPI3 du STM32, et le configurer en mode Full-Duplex Master.

### Tests

#### MCP23S17

Nous allons écrire un driver pour le MCP23S17. L'adresse du la puce est 0x40 pour écrire et 0x41 pour lire. On met dans un couple de fichiers MCP_functions, les prototypes et fonctions du GPIO Expander.
On commence alors par une intialisation du MCP23S17 ainsi qu'une fonction pour écrire et lire dans des registres.

[MCP_functions.h](https://github.com/ton-utilisateur/ton-repository/blob/main/src/example.txt)
[MCP_functions.c](https://github.com/ton-utilisateur/ton-repository/blob/main/src/example.txt)

![MCP_functions](https://github.com/user-attachments/assets/f640d46a-4480-46e0-9a9f-66c1758ee94d)

On active le Chip Select pour écrire dans les registres et on le désactive quand on ne l'utilise plus.

#### LEDS

Nous allons maitenant écrire un driver pour contrôler les Leds, dans le couple de fichiers led. Nous allons définir les leds comme un structure contenant son registre associé, son pin et son état. Les registres pour contrôler les leds sont les registres A et B

[MCP_functions.h](https://github.com/ton-utilisateur/ton-repository/blob/main/src/example.txt)
[MCP_functions.c](https://github.com/ton-utilisateur/ton-repository/blob/main/src/example.txt)

![structure_led](https://github.com/user-attachments/assets/306b2904-ca9e-46cb-8f1e-8a7846050b24)

On commence par une initialisation des leds, puis on écrit une fonction pour allumer une led ou toutes les leds, et on fait de même pour les éteindre


