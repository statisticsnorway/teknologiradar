
# SSBs teknologiradar

En teknologiradar skal gi veiledning på egnethet av prefererte teknologier. Den har en rolle både i å beskrive nåværende praksis og erfaringer samtidig som den veileder til fremtidige teknologivalg. Den er vedlikeholdt for og av utviklere i IT avdelingen i SSB. Alle utviklere er oppfordret til å holde radaren oppdatert, om det er en ny teknologi som burde legges til, eller en som burde fases ut. Forslagene vurderes løpende av Tech Lead forumet i SSB. Radaren er hostet på SSBs Backstage instans: [SSBs teknologiradar](https://backstage.intern.ssb.no/tech-radar)

## Hvordan bidra med forslag til teknologier

Radarløsningen vi bruker genererer radaren automatisk ved å lese en [fil](./teknologiradar.json) som ligger i dette repoet. Hvis du ønsker å bidra, kan du sende forslag til teknologier ved å klone dette repoet, lage en ny *branch*, gjøre endringer i filen, og deretter lage en PR. Tech lead forum vil vurdere forslaget og publisere de nye endringene i repoets *main branch*.

For de som ikke er kjent med denne typen arbeidsflyt, kalt [GitHub flow](https://docs.github.com/en/get-started/quickstart/github-flow), så er det også mulig å sende forslag til oss på [<img src="https://img.shields.io/badge/Slack-4A154B?style=for-the-badge&logo=slack&logoColor=white" alt="Slack logo for lenke til #adr kanal.">](https://ssb-norge.slack.com/archives/C02NRC2V83Z)

Valg av teknologier i produktteamene i SSB skal gjøres innenfor rammene av våre ADRer. Om det skal bli satt nye standarder eller gjøres mer definerende teknologivalg på høyere nivå skal dette først forankres i en ADR før det gjøres oppdateringer til anbefalningene i denne radaren. Om det er tvil rundt et definerende valg skal det konfereres med seksjon for it-arkitektur før det gjøres endringer. Om en oppdatering til teknologiradaren gjøres på grunnlag av en ADR skal denne lenkes til i PRen.

---

## Informasjon om filstrukturen

[Strukturen til JSON fila er definert her.](https://github.com/backstage/community-plugins/tree/main/workspaces/tech-radar/plugins/tech-radar#tech-radar-data-model) I skrivende stund har vi ingen validering på formatet så det gjelder å være forsiktig og teste endringer manuelt. Herme gjerne etter formatet til eksisterende innlegg.

---

## Hvordan lese teknologiradaren

Radaren består av tre ringer og er delt inn i fire kvadranter. Disse er representert av verdiene i kolonnene `ring` og `quadrant` i *json* fila over.

Inndelingen vi benytter er *veldig* inspirert av [Oslo Origo sin tech-radar](https://developer.oslo.kommune.no/teknologiradar/index.html).

### Teknologiene
Teknologiradaren skal være en samling av de sentrale teknologiene som er aktuelle for produktteamene i SSB. Dette er teknologier som brukes i produksjon, eller teknologier som evalueres for bruk i produksjonssetting. Hvis teknologien ikke lenger brukes eller utforskes av noe team i dag, burde den derfor fjernes fra teknologiradaren.

### Ringene
Hver *ring* kan sees på som et modenhetsnivå for teknologien. Å plassere en teknologi innenfor et modenhetsnivå vil alltid være en krevende øvelse, og hvor kompetanse og erfaring vil være en viktig faktor i vurderingen.

`Bruk` \
Teknologier som ligger i denne *ringen* har høyeste modenhetsnivå. Teknologier innenfor denne ringen har vært testet og vurdert for konkrete bruksområder, og er allerede satt i produksjon hos et eller flere teams. Produktteamene kan ta disse i bruk for nye løsninger. Hvis det er føringer eller begrensninger på bruken av disse teknologiene skal det dokumenteres i beskrivelsen i teknologiradaren. **Team som velger å ta i bruk disse teknologiene må fortsatt gjøre egne vurderinger knyttet til forretningsbehov, informasjonssikkerhet og arkitekturbeslutninger.**

`Vurder` \
Teknologier i denne *ringen* har ikke stor nok utbredelse. Det kan være mange grunner til det, både positive og negative. Som regel vil det være noe usikkerhet knyttet til modenheten på disse teknologiene, og om vi ønsker å bruke disse til fremtidige løsninger. Det anbefales derfor at teammedlemmer eksperimenterer med disse og foretar grundige vurderinger før de eventuelt tas i bruk. En teknologi burde ikke ligge her for lenge ettersom målet vil være å plassere den i "Bruk" eller "Avstå" om den har blitt produksjonssatt. Alternativt kan den flytte den ut av teknologiradaren om den ikke lenger er aktuell for bruk i SSB.

`Avstå` \
Teknologiene i denne ringen er produksjonssatt i SSB, men vi ønsker ikke å bygge nye systemer med disse teknologiene. Det er knyttet stor usikkerhet til teknologiene i denne *ringen*. Det kan være flere grunner til at vi ikke ønsker å ta teknologien i bruk i fremtiden. F.eks. at teknologien er på vei "ut av markedet". Selv om vi ønsker å bevege oss bort fra denne teknologien på SSB betyr ikke det at det alltid er feil valg. Men om man ønsker man å bruke denne teknologien selv om den står i avstå, burde man ha svært gode argumenter for det. Om en teknologi flyttes til "Avstå" skal det beskrives et alternativ som nå brukes for nye systemer som møter samme behovene som denne teknologien.
At en teknologi flyttes til Avstå betyr ikke at det nå er en forventning om at alle systemer som allerede bruker teknologien skal migreres øyeblikkelig. Det er en anbefalning om å ikke bruke teknologien for nye løsninger, og at det nå burde eksistere en pragmatisk plan for utfasing av teknologien i eksisterende systemer. Denne vurderingen gjøres av teamene som eier systemene.

### Kvadrantene 

*Kvadranetene* i radaren tilsvarer en kategori som avgrenser teknologienes bruksområde.

`Programmering` \
Kodespråk, rammeverk, biblioteker, testrammeverk osv.

`DevOps` \
Verktøy og systemer som ikke inngår i selve kodeartifakten, men bidrar til kvalitetskontroll, utrulling, monitorering osv.

`Infrastruktur` \
Tredjeparts systemer/plattform som programvaresystemer utviklet i SSB er avhengig av under kjøretid.

`Sikkerhet` \
Alt som er relatert til sikkerhet.

### Beste praksis for å beskrive en teknologi i radaren

Beskrivelsene burde bestå i det minste av:

1. En kort introduksjon av hvilket problem teknologien løser, og hvordan den skal brukes.
2. Styker og svakheter ved teknologien som fremhever hvorfor den er valgt.
3. En lenke til hvor man finner mer informasjon om teknologien.
4. En lenke til dokumentasjon om begrensninger for bruk i SSB om aktuelt.
5. Eventuelle erfaringer fra eksperimentering eller produksjonssatt bruk i SSB.
