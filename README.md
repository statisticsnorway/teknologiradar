# SSB's teknologiradar

I dette repoet vil vi samle teknologier som skal være en del av SSBs teknologiradar. På nåværende tidspunkt bruker vi [Thoughtworks](https://www.thoughtworks.com/radar) radarløsning for å visualisere vår egen radar. Alle i SSB kan bidra med forslag til teknologier. Forlagene vil vurderes løpende av en redaksjon bestående av personer fra flere fagområder i SSB. Sjekk ut radaren her: [SSBs teknologiradar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fstatisticsnorway%2Fteknologiradar%2Fmain%2FSSB%2520-%2520Teknologiradar.csv)

### Hvordan bidra med forslag til teknologier:

Radarløsningen vi bruker genererer radaren automatisk ved å lese en *csv* fil som ligger i dette repoet. Hvis du ønsker å bidra, kan sende forslag til teknologier ved å klone dette repoet, lage en ny *branch*, gjøre endringer i *csv* filen, og deretter lage en *pull request* (PR). Redaksjonen vil vurdere forslaget og publisere de nye endringene i repoets *main branch*. For de som ikke er kjent med denne typen arbeidsflyt kalt [GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow), så er det også mulig å sende forslag til teknologier i denne slackkanalen: [Slack kanal for SSBs teknologiradar](https://ssb-norge.slack.com/archives/C02NRC2V83Z)

---

### Informajson om CSV filstruktur:

For å gjøre endringer i *csv* filen, må man følge en fastsatt struktur. Nedenfor ser du en visuell fremstilling av *csv* filens *header* og hvilke verdier som aksepteres i de forskjellige kolonnene. Nærmere beskrivelse av verdiene finner du i seksjonene lenger ned på siden.
*Kolonnene i csv filen må skilles med et komma tegn.*

| name 	| ring 	| quadrant 	| isNew 	| description 	|
|-------|-------|-----------|---------|---------------|
|Text |`Ta i bruk`<br />`Prøv ut`<br />`Vurder`<br />`Avvent`|`Datainnsamling - lagring`<br />`Klargjøring`<br />`Analyse - formidling`<br />`Utvikling - infrastruktur`|`TRUE`<br />`FALSE`|"Text"|

---

### Beskrivelse av verdiene i *ringene* i teknologiradaren

Radaren består av fire ringer:
<img src="https://github.com/statisticsnorway/teknologiradar/blob/mehran/radar.png" alt="teknologiradar" width="150"/>

Hver *ring* kan sees på som et modenhetsnivå for teknologien.

![Ringer i teknologiradaren](https://github.com/statisticsnorway/teknologiradar/blob/mehran/rings.png)

`Ta i bruk` \
Teknologier som ligger i denne *ringen* har høyeste modenhetsnivå. Produktteamene i SSB bør **ta i bruk** disse teknologiene/verktøyene i produksjonsmiljøet. Teknologier innenfor dette modenhetsnivået har vært testet og vurdert for konkrete bruksområder, og er mest sannsynlig allerede satt i produksjon hos et eller flere teams. Team som velger å ta i bruk disse teknologiene må fortsatt gjøre egne vurderinger knyttet til forretningsbehov, informasjonssikkerhet og arkitekturbeslutninger.

`Prøv ut` \
Teknologier i denne *ringen* har stor utbredelse hos eksterne miljøer, men er ikke godt nok kjent i SSB. Det anbefales at teamene *prøver ut* disse teknologiene for å se om de vil dekke behovene. Det kan f.eks. være fornuftig å få erfaring med disse i et stagingmiljø, før man vurderer å rulle disse ut i produksjonsmiljøet.

`Vurder` \
Teknologier i denne *ringen* har ikke stor nok utbredelse. Det kan være mange grunner til det, både positive og negative. Som regel vil det være noe usikkerhet knyttet til modenheten på disse teknologiene. Det anbefales derfor at teammedlemmer *vurderer* disse individuelt, f.eks. lokalt eller i et *devmiljø*, slik at man ikke bruker for mye tid på å utvikle CI/CD pipelines (staging/prodmiljø) hvor disse inngår.

`Avvent`
Teknologier i denne *ringen* har enten for lav modenhetsnivå eller er på vei "ut av markedet". Det anbefales ikke at man vurderer disse teknologiene for å løse sine behov.
