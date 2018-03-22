# ESP32 på devkit v1 från DOIT
Först, varför publicerar jag detta? -Jo, för att just de billiga ESP-WROOM-32 utvecklingskorten från t.ex. Asien (55 SEK på t.ex. Banggood) verkar säljas bort till förmån för nya serier eller så rör det sig om piratkopierade utvecklingskort med äkta ESP-chip.

## Vad skiljer?
Det billiga utvecklingskortet märkt "ESP32 DEVKIT V1 DOIT" har 2x18 pinout (36pin) är _obefintligt_ dokumenterat på Internet/Banggood/DOIT. Det kortet från DOIT som har 2x15 (30-pin) är väldokumenterat. Båda utvecklingskorten bär ett ESP-WROOM-32 chip som är väldokumenterat. Problemet med det odokumenterade utvecklingskortet diskuteras bl.a som ett issue på Github https://github.com/espressif/arduino-esp32/issues/544 senast 3 mars 2018 och på banggood https://forum.banggood.com/forum-topic-258596.html?page=2.

## Pin out/Pin map
Problemet handlar om mappningen mellan _pinout_ (anslutningspinnarna till kortet) och ESP32-pinnarna på chipet.

## Pinout - 2x15 pins versionen
Lägg märke till att andra pinnen till höger på 2x15 kortet också är GND medan på 2x18 kortet är det CLK.

<img src="images/pinoutDOIT32devkitv1.png">
<img src="https://github.com/johansundstrom/esp32_doit_devkit_v1/blob/master/images/esp32-banggod.jpg">

## Pinout - 2x18 pins versionen från bl.a. Banggood
Lägg märke till att andra pinnen till höger på 2x15 kortet också är GND medan på 2x18 kortet är det CLK. Det är också större avstånd mellan de diskreta komponenterna och ESP-chipet.

<img src="images/esp32-36pins_versionen.jpg">

### Hanteringen av pinnarna
Avkodning av samtliga pinnar på 2x18pins versionen.

#### I2C 
Biblioteket Wire.h använder pin D21 (SDA) och D22 (SCL) på 2x18 kortet.

## ESP32 - ESP-WROOM-32?
ESP32 är chipet från Espressif. ESP-WROOM-32 är modulen som chipet sitter på.

## Block Diagram
<img src="images/esp32-block.jpg">

## ESP-WROOM-chippet
Inga tveksamheter finns vad gäller modulen som Tensilica-CPU'n sitter på. Enligt denna dokumentation får man utgå ifrån att pinnarna från ESP-WROOM-32-chippen korresponderar mot Modulen från DOIT enligt följande


