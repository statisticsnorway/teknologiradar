# SSB's teknologiradar

Repo for å samle relevante teknologier som skal være en del av SSBs teknologiradar. På nåværende tidspunkt bruker vi Thoughtworks radarløsning for å visualisere vår egen radar basert på en CSV fil som ligger i dette repoet. Alle i SSB kan bidra med forslag til teknologier. Forlagene vil vurderes løpende av redaksjonen for teknologiradaren. Sjekk ut radaren her: [SSBs teknologiradar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fstatisticsnorway%2Fteknologiradar%2Fmain%2FSSB%2520-%2520Teknologiradar.csv)


### CSV filstruktur (header):

| name 	| ring 	| quadrant 	| isNew 	| description 	|


<strong>name</strong> = Navn på teknologien

<strong>ring</strong> = `Ta i bruk`, `Prøv ut`, `Vurder`, `Avvent`

<strong>quadrant</strong> = `Datainnsamling - lagring`, `Klargjøring`, `Analyse - formidling`, `Utvikling - infrastruktur`

<strong>isNew</strong> = `TRUE` eller `FALSE`

<strong>description</strong> = Teksten må omsluttes med anførselstegn (""). HTML tagger er lov. Eksempel: `"Dette er en beskrivelse <br> Mer info her:<a href=""https://example.com"">Eksempel</a>"`

### Hvordan sende inn forslag:

Du sender forslag til endringer ved å lage en "pull request" etter at du har gjort endringer i CSV filen basert på informasjonen over. Redaksjonen vil vurdere forslaget og gi deg tilbakemelding på om forlaget er godkjent eller ikke. Det er kun redaksjonen som publiserer endringer i teknologiradaren.

### Hva betyr de forskjellige *ringene* i teknologiradaren

*Ringene*, som også kan sees på som modenhetsnivåer, er oversatt til norsk fra Thoughtworks sin radar:

`Ta i bruk`
Produktteam i SSB bør **TA I BRUK** denne teknologien/verktøyet. Teknologier innenfor dette modenhetsnivået har vært testet og vurdert for konkrete bruksområder, og er mest sannsynlig allerede satt i produksjon. Team som velger å ta i bruk disse teknologiene må fortsatt gjøre egne vurderinger knyttet til forretningsbehov, informasjonssikkerhet og arkitektur.

`Prøv ut` \
`Vurder` \
`Avvent`
