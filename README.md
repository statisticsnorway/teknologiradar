# SSB's teknologiradar

Repo for collecting relevant technologies for Statistics Norway's techology radar. As for now we are utilizing Thoughtworks in-built radar to visualize our tech based on a .csv file provided in this repo. You can add new technologies to the csv file, just follow the guidelines provided below. Visit our radar here: [SSBs teknologiradar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fstatisticsnorway%2Fteknologiradar%2Fmain%2FSSB%2520-%2520Teknologiradar.csv)

### CSV file header structure:

<strong>name,ring,quadrant,isNew,description</strong> 

`name = Can be anything`

`ring = 'Ta i bruk', 'Prøv ut', 'Vurder', 'Avvent'`

`quadrant = 'Datainnsamling - lagring', 'Klargjøring', 'Analyse - formidling', 'Utvikling - infrastruktur'`

`isNew = TRUE or FALSE`

`description = A text string inclosed in "". HTML tags are allowed.`

### Usage:

After comitting changes to the csv file, go to: [SSBs teknologiradar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fstatisticsnorway%2Fteknologiradar%2Fmain%2FSSB%2520-%2520Teknologiradar.csv)
<br><br>
*PS. Sometimes, changes made to the csv file are not instantly visible in the radar, most likely caused by some type of caching mechanism. Just wait a few minutes for changes to propagate and reload the radar.*

#### Next:
In the future, we will probably move on to self-hosted BYOR (Bring Your Own Radar) provided here: [BYOR](https://github.com/thoughtworks/build-your-own-radar).
