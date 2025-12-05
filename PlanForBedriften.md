# Kort plan — 1-ukes MVP for én person

Formål: Rask, fungerende løsning som lar kunder sende inn en sak og gir bedriften et enkelt admin-view for oppfølging.

Hva leveres (MVP):
- Ett-sides innsending: velg tjeneste (1–2), beskrivelse, kontaktinfo, opptil 2 vedlegg.
- Backend: minimal API for opprettelse og henting av saker, enkel fil-lagring.
- Admin: enkel liste med søk/filtrering + detaljvisning for å endre status.
- E-postbekreftelse til kunde ved innsending.

Hva som IKKE er med i MVP:
- Avanserte roller/tilganger, 2FA, omfattende filtrering eller SLA-automatisering.

Forslag til teknisk stack (minimalt):
- Frontend: React + enkel CSS (eller Tailwind).
- Backend: Node.js + Express, multer for opplasting.
- Database: SQLite eller PostgreSQL (for rask launch kan SQLite brukes lokalt).
- Fil-lagring: lokalt for MVP, bytt til S3 senere.

En uke — grovt dag-for-dag:
1. Dag 1: Avklar detaljer og skjemafelt; opprett repo og grunnstruktur.
2. Dag 2: Backend: API-endepunkter (POST /cases, GET /cases, GET /cases/:id) + DB.
3. Dag 3: Frontend: skjema + klientvalidering + opplasting.
4. Dag 4: Admin: liste og detaljvisning; enkel auth.
5. Dag 5: Testing, feilretting, e-post, README og deploy-til-staging.

Akseptkriterier (enkle):
- Kunde kan sende inn sak med kontaktinfo og vedlegg.
- Sak vises i admin-liste og kan markeres som «under behandling» / «ferdig».
- Innsending gir e-postbekreftelse til kunden.

Neste steg (en handling):
- Velg om jeg skal: (A) lage et prosjekt-skjelett i repoen, eller (B) generere en teknisk backlog (issues). Skriv "A" eller "B".