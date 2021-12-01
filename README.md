# SSB's teknologiradar

Repo for å samle relevante teknologier som skal være en del av SSBs teknologiradar. På nåværende tidspunkt bruker vi Thoughtworks radarløsning for å visualisere vår egen radar basert på en CSV fil som ligger i dette repoet. Alle i SSB kan bidra med forslag til teknologier. Forlagene vil vurderes løpende av redaksjonen for teknologiradaren. Sjekk ut radaren her: [SSBs teknologiradar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fstatisticsnorway%2Fteknologiradar%2Fmain%2FSSB%2520-%2520Teknologiradar.csv)

### Hvordan sende inn forslag:

Du kan sende forslag til teknologier ved å lage en "pull request" etter at du har gjort endringer i CSV filen basert på informasjonen under. Redaksjonen vil vurdere forslaget på en åpen måte, men det er kun redaksjonen som kan publiserer endringer i teknologiradaren. Det vil også være mulig å sende forslag til teknologier på SSBs Slack (Slack-kanal må opprettes)

---

### CSV filstruktur (header):

| name 	| ring 	| quadrant 	| isNew 	| description 	|
|-------|-------|-----------|---------|---------------|
|Text |`Ta i bruk`<br />`Prøv ut`<br />`Vurder`<br />`Avvent`|`Datainnsamling - lagring`<br />`Klargjøring`<br />`Analyse - formidling`<br />`Utvikling - infrastruktur`|`TRUE`<br />`FALSE`|"Text"|

<strong>Feltene må separeres med komma tegn (,).</strong>


### Hva betyr de forskjellige *ringene* i teknologiradaren

*Ringene*, som også kan sees på som modenhetsnivåer, er oversatt til norsk fra Thoughtworks sin radar:

`Ta i bruk` \
Produktteam i SSB bør **TA I BRUK** denne teknologien/verktøyet. Teknologier innenfor dette modenhetsnivået har vært testet og vurdert for konkrete bruksområder, og er mest sannsynlig allerede satt i produksjon. Team som velger å ta i bruk disse teknologiene må fortsatt gjøre egne vurderinger knyttet til forretningsbehov, informasjonssikkerhet og arkitektur.

`Prøv ut` \

`Vurder` \
`Avvent`
