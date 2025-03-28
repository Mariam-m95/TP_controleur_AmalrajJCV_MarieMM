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

Nous allons écrire un driver pour configurer les leds du GPIO expander. On commence alors par une intialisation de toutes les leds. L
