# SSB's teknologiradar

Repo for collecting relevant technologies for Statistics Norway's techology radar. As for now we are utilizing Thoughtworks in-built radar to visualize our techs based on a .csv file provided in this repo. You can add new technologies to the csv file, just follow the guidelines provided below.

### CSV file header structure:

<strong>name,ring,quadrant,isNew,description</strong> 

`name = Can be anything`

`ring = 'Ta i bruk', 'Prøv ut', 'Vurder', 'Avvent'`

`quadrant = 'Datainnsamling - lagring', 'Klargjøring', 'Analyse - formidling', 'Utvikling - infrastruktur'`

`isNew = TRUE or FALSE`

`description = A text string inclosed in "". HTML tags are allowed.`

### Usage:

After comitting to the csv file, Go to: https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fstatisticsnorway%2Fteknologiradar%2Fmain%2FSSB%2520-%2520Teknologiradar.csv

