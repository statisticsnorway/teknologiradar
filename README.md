![](https://tokei.rs/b1/github/statisticsnorway/teknologiradar)
# [SSBs teknologiradar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fstatisticsnorway%2Fteknologiradar%2Fmain%2FSSB%2520-%2520Teknologiradar.csv)

I dette repoet vil vi samle teknologier som skal være en del av SSBs teknologiradar. På nåværende tidspunkt bruker vi [Thoughtworks](https://www.thoughtworks.com/radar) radarløsning for å visualisere vår egen radar. Alle i SSB kan bidra med forslag til teknologier. Forlagene vil vurderes løpende av en redaksjon bestående av personer fra flere fagområder i SSB. Sjekk ut radaren her: [SSBs teknologiradar](https://radar.thoughtworks.com/?sheetId=https%3A%2F%2Fraw.githubusercontent.com%2Fstatisticsnorway%2Fteknologiradar%2Fmain%2FSSB%2520-%2520Teknologiradar.csv)

### Hvordan bidra med forslag til teknologier:

Radarløsningen vi bruker genererer radaren automatisk ved å lese en [*csv* fil](https://github.com/statisticsnorway/teknologiradar/blob/main/SSB%20-%20Teknologiradar.csv) som ligger i dette repoet. Hvis du ønsker å bidra, kan sende forslag til teknologier ved å klone dette repoet, lage en ny *branch*, gjøre endringer i *csv* filen, og deretter lage en *pull request* (PR). Redaksjonen vil vurdere forslaget og publisere de nye endringene i repoets *main branch*.
For de som ikke er kjent med denne typen arbeidsflyt, kalt [GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow), så er det også mulig å sende forslag til teknologier i denne slackkanalen: [SSBs teknologiradar på Slack](https://ssb-norge.slack.com/archives/C02NRC2V83Z)

---

### Informajson om CSV filstruktur:

For å gjøre endringer i [*csv* filen](https://github.com/statisticsnorway/teknologiradar/blob/main/SSB%20-%20Teknologiradar.csv), må man følge en fastsatt struktur. Nedenfor ser du en visuell fremstilling av *csv* filens *header* og hvilke verdier som aksepteres i de forskjellige kolonnene. Nærmere beskrivelse av hva disse verdiene betyr, finner du i seksjonene lenger ned på siden. \
*NB: Kolonnene/feltene i csv filen må skilles med et komma tegn og det kan ikke være noe mellomrom (whitespace) mellom kolonnene. Verdiene i kolonnene ring, quadrant og isNew er case-sensitive.*

| name 	| ring 	| quadrant 	| isNew 	| description 	|
|-------|-------|-----------|---------|---------------|
|Text |`Ta i bruk`<br />`Prøv ut`<br />`Vurder`<br />`Avvent`|`Datainnsamling - Lagring`<br />`Klargjøring`<br />`Analyse - Formidling`<br />`Utvikling - Infrastruktur`|`TRUE`<br />`FALSE`|"Text og/eller HTML"|

**Eksempel:**
```
Tech1,Vurder,Klargjøring,TRUE,"En kuul tech!<a href=""https://eksempel.no/"">Tech1</a>"
```
---

### Hvordan lese teknologiradaren

Radaren består av fire ringer og er delt inn i fire kvadranter. Disse er representert av verdiene i kolonnene `ring` og `quadrant` i *csv* tabellen over.

<img src="https://github.com/statisticsnorway/teknologiradar/blob/main/radar.png" alt="teknologiradar" width="150"/>

### Beskrivelse av *ringene* i teknologiradaren

Hver *ring* kan sees på som et modenhetsnivå for teknologien. Å plassere en teknologi innenfor et modenhetsnivå vil alltid være en krevende øvelse, og hvor kompetanse og erfaring vil være en viktig faktor i vurderingen.  

![Ringer i teknologiradaren](https://github.com/statisticsnorway/teknologiradar/blob/main/rings.png)

`Ta i bruk` \
Teknologier som ligger i denne *ringen* har høyeste modenhetsnivå. Produktteamene i SSB bør ta i bruk disse teknologiene/verktøyene i produksjonsmiljøet. Teknologier innenfor dette modenhetsnivået har vært testet og vurdert for konkrete bruksområder, og er mest sannsynlig allerede satt i produksjon hos et eller flere teams. **Team som velger å ta i bruk disse teknologiene må fortsatt gjøre egne vurderinger knyttet til forretningsbehov, informasjonssikkerhet og arkitekturbeslutninger.**

`Prøv ut` \
Teknologier i denne *ringen* har stor utbredelse hos eksterne miljøer, men er ikke godt nok kjent i SSB. Det er generelt liten usikkerhet knyttet til disse teknologiene. Det anbefales at teamene prøver ut disse teknologiene. Det kan f.eks. være fornuftig å få erfaring med disse i et stagingmiljø, før man vurderer å rulle disse ut i produksjonsmiljøet.

`Vurder` \
Teknologier i denne *ringen* har ikke stor nok utbredelse. Det kan være mange grunner til det, både positive og negative. Som regel vil det være noe usikkerhet knyttet til modenheten på disse teknologiene. Det anbefales derfor at teammedlemmer eksperimenterer med disse individuelt, f.eks. lokalt eller i et *devmiljø*. På denne måten kaster man ikke bort verdifull tid  på å utvikle CI/CD pipelines (staging/prodmiljø), før man vet noe mer konkret om teknologien.

`Avvent` \
Det er knyttet stor usikkerhet til teknologiene i denne *ringen*. Det kan være flere grunner til at modenheten vurderes som lav. F.eks. at teknologien er på vei "ut av markedet". Det anbefales å vente med å ta i bruk disse teknologiene.

### Beskrivelse av *kvadrantene* i teknologiradaren

*Kvadranetene* i radaren tilsvarer en kategori som avgrenser teknologienes bruksområde. Kategoriene gjenspeiler SSBs forretningsområdet slik det er skissert i SSBs virksomhetsmodell.

`Datainnsamling - Lagring` \
Denne kategorien skal dekke alle teknologier og verktøy som faller inn under datainnsamling og datalagring.

`Klargjøring` \
Denne kategorien omfatter alle teknologier og verktøy som inngår i datatransformasjoner og dataprosessering.

`Analyse - Formidling` \
Denne kategorien omfatter teknologier og verktøy innenfor dataanalyse, datautforsking og dataformidling

`Utvikling - Infrastruktur` \
Denne kategorien er tiltenkt all annen teknologi fra et IT-utviklings og infrastruktur perspektiv.

### Syngliggjøre endringer i teknologiradaren

Det er mulig å visualisere endringer i teknologiradaren. Dette kan være nyttig når man f.eks. ønsker å vise hvilke teknologier som er helt nye eller om en eksisterende teknologi i radaren har endret modenhetsnivå (*ring*). Eller at man ønsker å visualisere at det ikke har vært noen endringer.

Ved å sette kolonnen `isNew` med boolsk verdi `TRUE` eller `FALSE` i csv filen, kan man nettopp styre dette. Teknologiene som vises i radaren vil få forskjellige *ikoner* avhengig av hvilken verdi man setter.

![isNew](https://github.com/statisticsnorway/teknologiradar/blob/main/isNew.png)

### Beste praksis for å beskrive en teknologi i radaren

Det er viktig at radaren ikke fylles opp med for mange teknologier slik at den blir uoversiktlig. Det er også viktig at det er gode beskrivelser av teknologiene som legges inn, slik at ansatte i SSB føler at de får nytte av radaren ved at de forstår hensikten med den utvalgte teknologien. Denne typen informasjon skal legges inn i **description** feltet i *csvfilen*. Vi ønsker at alle beskrivelser begynner med:

1. En kort introduksjon av hvilket problem teknologien løser.
2. Styker og svakheter ved teknologien som fremhever hvorfor den er valgt.
3. En lenke til hvor man finner mer informasjon om teknologien.
