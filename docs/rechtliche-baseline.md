# Rechtliche Baseline vor dem Launch – endia.de

```
Status:  Entwurf – nicht verbindlich, keine Rechtsberatung; Übernahme entscheidet Thomas
Stand:   2026-11-28
Anlass:  EXT-KG-ENDIA-20261127-001 (Research Candidate RES-20260918-C5EDAF53, nicht-kanonisch)
Siehe:   docs/pruefnotiz-rechtstexte-herkunft.md (Herkunft der Rechtstexte, EXT-KG-ENDIA-20261127-002)
```

Diese Baseline hält die Entscheidungen fest, die **vor dem Bau** billig und nachträglich teuer
sind. Sie betrifft ausschließlich Technik, Datenverarbeitung und Gestaltung der Website – der
fiktionale Kanon der Endia-Trilogie bleibt unberührt. Sie ist kein geprüfter Rechtstext; vor
dem Launch ist eine juristische Prüfung nötig.

Der gemeinsame Nenner aller Punkte: **Datenminimierung**. Ob es Konten, Analytics,
Kommentare oder eingebettetes Bewegtbild gibt, entscheidet über die Pflichten – nicht die
Länge späterer Rechtstexte.

## (a) Konten, Rechtsgrundlage und Altersgate

- Konten – falls es überhaupt welche gibt – ausschließlich auf **Art. 6 Abs. 1 lit. b oder
  lit. f DSGVO** stützen (Vertrag bzw. berechtigtes Interesse), nicht auf Einwilligung. Damit
  greift **Art. 8 DSGVO** (elterliche Einwilligung, in Deutschland Altersgrenze 16) für die
  Kontoanlage nicht. Die Legal Registry hält das für NOXIA/SSF schon so (Art. 6 Abs. 1 lit. b/f).
- **Kein Altersgate per Selbstauskunft.** Geburtsdatums- oder Ja/Nein-Abfragen werden
  empirisch durchgängig umgangen, taugen nicht als Age Assurance und schaffen einen
  zusätzlichen Verarbeitungstatbestand. Wirksamer sind sichere Voreinstellungen.
- **Sichere Defaults statt Abfragen:** keine Profilbildung, keine öffentliche Sichtbarkeit von
  Profilen oder Beiträgen, keine Standortdaten, keine Weitergabe an Dritte – jeweils als
  Voreinstellung. Grund: Jugendliche übernehmen Voreinstellungen weitgehend und erkennen
  schlechte Defaults überwiegend nicht.
- Interaktive Funktionen (Kommentare, Community, nutzergenerierte Inhalte) sind die
  teuerste Einzelentscheidung – sie ziehen Moderation, Jugendschutzvorsorge und zusätzliche
  Verarbeitung nach sich. Vor dem Launch bewusst entscheiden, nicht nebenbei einbauen.

## (b) Abschnitt „Kinder und Jugendliche“ in der Datenschutzerklärung

**Nicht endia-intern umzusetzen.** Datenschutzerklärung und Nutzungsbedingungen liegen
kanonisch in `kueper-knowledge-graph/registry/legal/`; endia.de konsumiert sie (siehe
Prüfnotiz). Vor dem Launch als External Task an `KG`:

- eigener Abschnitt „Kinder und Jugendliche“ (fehlt bisher – nur zwei NOXIA-bezogene Stellen),
- Mindestalter bzw. die begründete Entscheidung dagegen, mit Rechtsgrundlage,
- Verbot von Profiling und Werbung gegenüber Minderjährigen (Erwägungsgrund 38 DSGVO),
- kindgerechte Kurzfassung in einfacher Sprache,
- Aufnahme von endia.de in den Geltungsbereich (Abschnitt 2 nennt endia.de bisher nicht).

## (c) Analytics standardmäßig aus

- **Voreinstellung: kein Analytics, kein Werbe-Tracking.** Nach **§ 25 Abs. 1 TDDDG** ist
  Speicherung auf oder Zugriff auf die Endeinrichtung nur mit Einwilligung zulässig – auch
  wenn die Daten nicht personenbezogen sind. Reichweitenmessung gehört nach der
  DSK-Orientierungshilfe nicht ohne Weiteres zum unbedingt erforderlichen Basisdienst.
- Technisch notwendige Session- und Authentifizierungs-Cookies bleiben nach **§ 25 Abs. 2
  TDDDG** einwilligungsfrei.
- Wird später doch Analytics eingesetzt: „Annehmen“ und „Ablehnen“ **gleichwertig** gestalten,
  kein Vorankreuzen, keine Weiternutzung-als-Einwilligung (EuGH C-673/17), kein Nudging und
  keine Dark Patterns. Ein gleichwertiger, klar beschrifteter Ablehnen-Knopf erfüllt TDDDG,
  WCAG und altersgerechtes Design in einem Schritt.

## (d) WCAG 2.2 AA als Definition of Done

- Jede UI-Komponente gilt erst als fertig, wenn sie **WCAG 2.2 AA** erfüllt (POUR: wahrnehmbar,
  bedienbar, verständlich, robust) – inklusive Tastaturbedienung, Kontrast, Zielgrößen,
  Fokussichtbarkeit und zugänglicher Formulare.
- Das ist eine **selbst gesetzte Qualitätsvorgabe**, keine festgestellte Pflicht (siehe
  Streitpunkte unten).
- Erzeugte Dokumente (PDF, Begleitmaterial) ebenfalls barrierefrei anlegen.

## (e) Impressum und Rechtstexte nur aus der Legal Registry

- Pflichtangaben kommen ausschließlich aus **`LEGAL:L3:impressum-master`**
  (`kueper-knowledge-graph/registry/legal/impressum-master.json`), gerendert, nicht kopiert.
  endia.de ist dort als Konsument (`SYS:KUEPER:endia`) eingetragen. Belegt in der Prüfnotiz.
- Keine eigenen Masterdaten in diesem Repository. Divergierende Pflichtangaben sind genau das
  Risiko, das die Registry verhindert. Änderungswünsche laufen als External Task an `KG`.
- Beide Texte haben Status `draft_productive` und sind nicht juristisch freigegeben.

## (f) JMStV-Kennzeichnung bei Bewegtbild oder Spielmodulen

- Der **JMStV** gilt für Telemedien und damit auch für diese Website. Die harten Pflichten –
  Jugendschutzbeauftragter nach § 7 JMStV, Alterskennzeichnung – knüpfen an
  **entwicklungsbeeinträchtigende oder jugendgefährdende Inhalte** an; eine reine Buchreihen-
  und Wissenswebsite löst sie nicht aus.
- Der novellierte JMStV gilt seit **1. Dezember 2025**; für Anbieter von Serien, Filmen und
  **Spielprogrammen** im Onlinebereich besteht seit **1. Juni 2026** eine Kennzeichnungspflicht
  mit Altersstufen und Deskriptoren. Dieses Datum ist überschritten. **Deshalb: Vor dem
  Einbetten von Bewegtbild- oder Spielmodulen (etwa aus NOXIA) die Kennzeichnungspflicht
  prüfen** – nicht erst danach.
- Ebenfalls prüfen, sobald Inhalte der Trilogie (Gewaltdarstellungen, „Digital
  Rebellion“-Motivik) aufbereitet werden oder nutzergenerierte Inhalte möglich sind.

## Streitige und zeitabhängige Punkte

Diese Punkte sind **nicht entschieden** und vor dem Launch erneut zu prüfen:

| Punkt | Stand |
|---|---|
| **BFSG-Anwendungsbereich** | Das BFSG erfasst nach § 1 Abs. 3 Nr. 5, § 2 Nr. 26 BFSG „Dienstleistungen im elektronischen Geschäftsverkehr“, definiert über das Hinwirken auf einen Verbrauchervertrag. Reine Informationswebsites fallen nicht darunter. Ob **kostenlose Angebote mit Nutzerkonten** erfasst sind, ist **ausdrücklich streitig**. Die Aussage „seit Juni 2025 müssen alle Websites barrierefrei sein“ ist so nicht korrekt. |
| **BITV 2.0** | Gilt für öffentliche Stellen des Bundes, nicht für private Anbieter – Orientierungsmaßstab, keine Pflichtnorm für endia.de. |
| **Kleinstunternehmen** | § 3 Abs. 3 BFSG nimmt Kleinstunternehmen (unter 10 Beschäftigte und höchstens 2 Mio. € Umsatz/Bilanzsumme) von den Dienstleistungspflichten aus – nur für Dienstleistungen, nicht für Produkte. Anwendbarkeit auf endia.de prüfen. |
| **EN 301 549 V4.1.1** | Am 2. September 2026 veröffentlicht, stellt die Web-Baseline von WCAG 2.1 AA auf **WCAG 2.2 AA** um. Die Amtsblatt-Zitierung (OJEU) war am 28.11.2026 **nicht bestätigt**; Quellen nannten Ende November bzw. Mitte Dezember 2026. Bis zur Zitierung bleibt V3.2.1 (2021, WCAG 2.1 AA) die zitierte Fassung, und es besteht keine gesetzliche Vermutungswirkung. **Vor dem Launch den aktuellen Zitierungsstand prüfen.** WCAG 2.2 AA jetzt zu bauen bleibt trotzdem sinnvoll, weil die Zielnorm vorliegt. |
| **Art. 8 DSGVO** | In Deutschland Altersgrenze 16. Relevant nur, soweit eine Verarbeitung doch auf Einwilligung gestützt wird – Punkt (a) vermeidet das bewusst. |
| **„maturity gap“** | Kognitive Kapazität erreicht Erwachsenenniveau um 16, psychosoziale Reife erst nach 18. Begründet die Default-Strategie, ist aber keine Rechtsnorm. |

## Prüfung vor dem Launch

- [ ] Entscheidung dokumentiert: Konten ja/nein, interaktive Funktionen ja/nein
- [ ] Rechtsgrundlage der Konten lit. b/f, kein Selbstauskunfts-Altersgate, Defaults gesetzt
- [ ] Analytics aus; falls aktiviert, gleichwertige Consent-Optionen ohne Nudging
- [ ] WCAG 2.2 AA je Komponente abgehakt; Zitierungsstand EN 301 549 geprüft
- [ ] Impressum/Datenschutz/Nutzungsbedingungen aus der Legal Registry gerendert
- [ ] External Task an `KG` für Punkt (b) gestellt, bevor endia.de online geht
- [ ] JMStV-Kennzeichnung geprüft, falls Bewegtbild oder Spielmodule eingebettet werden
- [ ] Juristische Prüfung der Rechtstexte veranlasst (Status bisher `draft_productive`)

Grundlage der Befunde (Einzelquellen mit Fundstellen): `kueper-knowledge-graph/research/candidates/RES-20260918-C5EDAF53.md`
– nicht-kanonischer Research Candidate. Diese Baseline ändert keinen Kanon und begründet keine
Ökosystem-Pflicht für andere Projekte.
