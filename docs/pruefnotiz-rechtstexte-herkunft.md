# Prüfnotiz: Herkunft der Rechtstexte und Minderjährigen-Lücke

```
Status:  Prüfnotiz – Feststellung, keine Änderung an Rechtstexten
Stand:   2026-11-28
Anlass:  EXT-KG-ENDIA-20261127-002 (Research Candidate RES-20260918-C5EDAF53, nicht-kanonisch)
Geprüft: kueper-knowledge-graph @ 8c4c40c (main, 27.11.2026), endia.de @ main (27.11.2026)
```

Geprüft wurde, woher endia.de Impressum und Datenschutzhinweise bezieht und ob die vom
Research Candidate behauptete Lücke zu Minderjährigen besteht. In diesem Schritt wurde
kein Rechtstext geändert.

## 1. Woher die Rechtstexte kommen

Kanonisches Repository ist **`kueper-knowledge-graph`**, nicht endia.de und nicht
`kueper.com`. Die Artefakte existieren – anders als im geprüften Checkout des Kandidaten:

| Artefakt | Pfad im KG | Inhalt |
|---|---|---|
| `LEGAL:L3:impressum-master` | `registry/legal/impressum-master.json` | Stammdaten des Verantwortlichen, Status `canonical`, Stand 19.07.2026; verweist auf `DOC:KUE:LEGAL-IMPRINT-DE`, `-PRIVACY-DE`, `-TERMS-DE` |
| Datenschutzerklärung | `registry/legal/datenschutz.de.md` | 194 Zeilen, Status `draft_productive`, ausdrücklich „Entwurf, kein geprüfter Rechtstext“ |
| Nutzungsbedingungen | `registry/legal/terms.de.md` | 109 Zeilen, derselbe Entwurfsstatus |

`registry/legal/README.md` legt die Regel fest: Websites pflegen keine eigenen Masterdaten
für Pflichtangaben, sondern konsumieren die kanonischen Daten und rendern sie lokal
(geplanter Endpunkt `https://kg.kueper.com/legal/impressum.json`). Die Verantwortlichen-Daten
der Datenschutzerklärung werden beim Build aus `impressum-master.json` aufgelöst.

**endia.de ist als Konsument eingetragen** (`SYS:KUEPER:endia` in `consumers`). Für endia.de
gilt damit: Impressum und Datenschutzhinweise ausschließlich aus der Legal Registry beziehen,
nicht lokal neu schreiben. Punkt (e) der Baseline (`docs/rechtliche-baseline.md`) ist dadurch
belegt. Technisch steht die Anbindung noch aus, weil endia.de bisher keinen Website-Code hat.

## 2. Die behauptete Lücke

Teilweise bestätigt. Die Datenschutzerklärung hat **keinen eigenen Abschnitt zu Kindern und
Jugendlichen**; Minderjährige kommen nur an zwei NOXIA-bezogenen Stellen vor:

- Abschnitt 7a: Schutzfilter gegen „Annäherung an Minderjährige mit Geheimhaltung“; Zweck
  „Schutz der Spieler und Dritter, insbesondere Minderjähriger“ (Art. 6 Abs. 1 lit. f, bei
  gesetzlicher Pflicht lit. c).
- Abschnitt 7a, Schluss: „Nutzung durch Minderjährige: Ob und ab welchem Alter NOXIA genutzt
  werden darf und ob eine Einwilligung der Erziehungsberechtigten nötig ist (Art. 8 DSGVO),
  ist vor Freigabe zu klären“ – also offen gestellt, nicht geregelt.

Im Einzelnen:

| Behauptung des Kandidaten | Befund |
|---|---|
| Kein Abschnitt zu Minderjährigen | **trifft zu** – nur die beiden NOXIA-Stellen oben, kein eigener Abschnitt und keine kindgerechte Fassung |
| Keine Aussage zum Mindestalter | **trifft zu** – weder in der Datenschutzerklärung noch in den Nutzungsbedingungen (§ 4 „Benutzerkonten“ nennt kein Alter) |
| Rechtsgrundlage für Konten fehlt | **trifft nicht zu** – Abschnitt 6 und 7a nennen Art. 6 Abs. 1 lit. b bzw. lit. f für Konto-, Session- und Spielfunktionen; eine Einwilligung wird für Konten nicht herangezogen, Art. 8 DSGVO greift insoweit nicht |
| Werbe-/Kommerzialisierungsverbot (EG 38 DSGVO) fehlt | **trifft zu** – kein Verbot von Profiling oder Werbung gegenüber Minderjährigen; Abschnitt 6 hält nur fest, dass es derzeit kein Analytics- und Werbe-Tracking gibt |

Weiterer Befund, der im Kandidaten nicht vorkommt: Die Datenschutzerklärung beschreibt in
Abschnitt 2 ausdrücklich nur die bestehenden Websites und nennt endia.de nicht. Sobald endia.de
online geht – erst recht mit Konten –, muss der Geltungsbereich erweitert werden.

## 3. Folge für endia.de

1. Keine eigenen Rechtstexte in diesem Repository. Impressum, Datenschutz und
   Nutzungsbedingungen kommen aus der Legal Registry.
2. Vor dem Launch als External Task an `KG`: Abschnitt „Kinder und Jugendliche“, Mindestalter
   bzw. Verzicht darauf samt Rechtsgrundlage, Verbot von Profiling und Werbung gegenüber
   Minderjährigen (EG 38 DSGVO), kindgerechte Kurzfassung sowie Aufnahme von endia.de in den
   Geltungsbereich. Punkt (b) der Baseline ist damit kein endia-interner Schritt.
3. Der Entwurfsstatus bleibt bestehen: Beide Texte sind `draft_productive` und nicht
   juristisch freigegeben. Diese Notiz ersetzt keine Rechtsprüfung.

Grundlage der Bewertung: `kueper-knowledge-graph/research/candidates/RES-20260918-C5EDAF53.md`
– nicht-kanonischer Research Candidate; die Rechtslage ist teils streitig und zeitabhängig.
