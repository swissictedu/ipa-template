# IPA Vorlage

Informatiklernende (EFZ) schliessen Ihre Ausbildung mit einer individuellen praktischen Abschlussprüfung (IPA) ab. Dabei sind umfangreiche Dokumentationsarbeiten notwendig. Diese Vorlage hilft dabei sich auf die Inhalte und Realisierung konzentrieren zu können und keine Inhalte zu vergessen. Mit dieser Vorlage ist es möglich, innert Minuten mit der produktiven Arbeit am IPA-Bericht zu beginnen.

## Funktionen

- Moderne TeX/LaTeX Umgebung [Tectonic](https://tectonic-typesetting.github.io/en-US/)
- Visual Studio Code mit [Remote Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
- Continuous Integration und Continuous Delivery mit Github Actions
- Integrierte Vorlage für den IPA Bericht
- Konfigurierbar über Variablen in `src/index.tex`

[![Screenshot](./res/ipa-template-vscode.png)](./res/ipa-template-vscode.png)

## Loslegen

1. Repository klonen
1. Ordner in Visual Studio Code mit installierter Erweiterung [Remote Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) öffnen
1. `src/index.tex` öffnen und <kbd>CTRL</kbd>+<kbd>ALT</kbd>+<kbd>b</kbd> oder über <kbd>CTRL</kbd>+<kbd>P</kbd> das Kommando `LaTeX Workshop: Build LaTeX project` aufrufen
1. `build/default/default.pdf` öffnen
1. Dokument ändern, die Vorschau des PDFs aktualisiert sich fortlaufend
1. Variablen in `src/index.tex` anpassen

## Kriteriennachweis

Dieser Abschnitt bezieht sich auf den [Standardkritierenkatalog](https://pk19.ch/wp-content/uploads/2021/11/Kriterienkatalog-Standardkriterien_2022.pdf) und dessen [Leitfaden](https://pk19.ch/wp-content/uploads/2021/11/QV-Leitfaden_2022.pdf). Unterhalb wird ein Bezug zwischen den Kriterien und dieser Vorlage hergestellt.

Der Status wird durch folgende Symbole definiert:

| Symbol | Bedeutung |
| ------ | --------- |
| ✔️ | Dieses Kriterium ist in der Vorlage beispielhaft umgesetzt. |
| ⏳ | Dieses Kriterium wird noch in der Vorlage umgesetzt. |
| ⚡ | Zu diesem Kriterium gibt es Hinweise und Beispiele, welche noch angepasst werden müssen. |
| ❌ | Dieses Kriterium kann nicht oder nur teilweise mit dem IPA-Bericht umgesetzt werden. |
| 🧑‍🎓 | Dieses Kriterium muss individuell in der Vorlage geprüft oder umgesetzt werden. |

### Teil A
 - [A1: Projektmanagement und Planung](#a1)
 - [A2: Wissensbeschaffung](#a2)
 - [A3: Zeitplan](#a3)
 - [A4: Konzeptionelle Umsetzung](#a4)
 - [A5: Projektumfeld: Systemgrenzen / Schnittstellen zur Aussenwelt](#a5)
 - [A6: Testkonzept](#a6)
 - [A7: Leistungsfähigkeit](#a7)
 - A8: Selbständiges Arbeiten
 - A9: Fachkenntnisse und Anwendungskompetenz
 - A10: Anwendung der Fachsprache
 - A11: Arbeits- und Fachmethodik
 - A12: Organisation der Arbeitsergebnisse
 - A13: IPA-Erfüllungsgrad

#### <span id="a1">A1</span>: Projektmanagement und Planung

| ID    | Anforderung | Referenz | Bemerkungen | Status |
| ----- | ----------- | -------- | ----------- | ------ |
| A1.1a | "Die gewählte Projektmanagement-Methode ist im Bericht benannt" | [`src/chapters/inform.tex`](src/chapters/inform.tex) | | ⏳ |
| A1.1b | "[..] und passt zum Auftrag;" | [`src/chapters/inform.tex`](src/chapters/inform.tex) | In den allermeisten Fällen lässt sich IPERKA anwenden und begründen. | 🧑‍🎓 |
| A1.2 | "Die gewählte Projektmanagement-Methode wurde in der praktischen Arbeit korrekt angewandt;" | | Dies lässt sich oftmals gut im Zeitplan erkennen, indem geprüft wird, ob die Aufgaben den passenden Phasen zugeordnet sind. | 🧑‍🎓 |
| A1.3 | "Die korrekte Anwendung der Projektmanagement-Methode ist im IPA-Bericht ersichtlich;" | [`src/index.tex`](src/index.tex) | Dies lässt sich gut am Inhaltsverzeichnis ablesen. | ✔️ |
| A1.4 | "Der Auftrag wurde ausgehend von der Aufgabenstellung weiter analysiert und verfeinert." | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | ⏳ |

#### <span id="a2">A2</span>: Wissensbeschaffung

| ID    | Anforderung | Referenz | Bemerkungen | Status |
| ----- | ----------- | -------- | ----------- | ------ |
| A2.1 | "Der Nachweis der Wissensbeschaffung ist durch Arbeitsjournal, Projektbericht oder Protokolle zu Fachgesprächen (HE, VF) dokumentiert;" | [`src/chapters/journal.tex`](src/chapters/journal.tex) | | ⏳ |
| A2.2 | "Wählte die Informationsquellen aufgabenbezogen aus;" | [`src/sources.bib`](src/sources.bib) | | 🧑‍🎓 |
| A2.3 | "Hat aus den gewählten Informationsquellen die relevanten Informationen identifiziert und genutzt (Transferleistung);" | | | ⏳ |
| A2.4 | "Die referenzierten Quellen sind existent und für Projektinvolvierte rekonstruierbar." | [`src/sources.bib`](src/sources.bib) | | 🧑‍🎓 |

#### <span id="a3">A3</span>: Zeitplan

| ID    | Anforderung | Referenz | Bemerkungen | Status |
| ----- | ----------- | -------- | ----------- | ------ |
| A3.1 | "Es wurde eine absolute Zeitachse definiert (Datum)." | [`src/chapters/timeplan.tex`](src/chapters/timeplan.tex) | | ⏳ |
| A3.2 | "Die Zeitachse hat eine vernünftige Auflösung (1, 2- oder 4-Stundenblöcke)." | [`src/chapters/timeplan.tex`](src/chapters/timeplan.tex) | | ⏳ |
| A3.3 | "Zweckmässige Tätigkeiten decken die ganze Arbeit ab." | [`src/chapters/timeplan.tex`](src/chapters/timeplan.tex) | | 🧑‍🎓 |
| A3.4 | "Die Reihenfolge der Tätigkeiten ist sinnvoll." | [`src/chapters/timeplan.tex`](src/chapters/timeplan.tex) | | 🧑‍🎓 |
| A3.5 | "Die Zeitaufwände für die Tätigkeiten wurden realistisch geplant." | [`src/chapters/timeplan.tex`](src/chapters/timeplan.tex) | | 🧑‍🎓 |
| A3.6 | "Der Soll/Ist-Vergleich ist transparent und korrekt." | [`src/chapters/timeplan.tex`](src/chapters/timeplan.tex) | | 🧑‍🎓 |

#### <span id="a4">A4</span>: Konzeptionelle Umsetzung

| ID    | Anforderung | Referenz | Bemerkungen | Status |
| ----- | ----------- | -------- | ----------- | ------ |
| A4.1 | "Es wurden Konzepte oder Modelle eingesetzt, um die Aufgabenstellung vereinfacht darzustellen." | [`src/chapters/inform.tex`](src/chapters/inform.tex) | | 🧑‍🎓 |
| A4.2 | "Es wurden Konzepte oder Modelle eingesetzt, um die Lösung vereinfacht darzustellen." | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | 🧑‍🎓 |
| A4.3 | "Teilsysteme sowie deren Abhängigkeiten sind identifiziert und dokumentiert." | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | 🧑‍🎓 |
| A4.4 | "Die Abbildung des Gesamtsystems orientiert sich an den ersten drei Punkten." | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | 🧑‍🎓 |

#### <span id="a5">A5</span>: Projektumfeld: Systemgrenzen / Schnittstellen zur Aussenwelt

| ID    | Anforderung | Referenz | Bemerkungen | Status |
| ----- | ----------- | -------- | ----------- | ------ |
| A5.1 | "Der Kandidat kennt die Abgrenzung seines Auftrages zum Umfeld" | [`src/chapters/inform.tex`](src/chapters/inform.tex) | | 🧑‍🎓 |
| A5.2 | "[..] Abgrenzung seines Auftrages zum Umfeld und kann dieses beschreiben." | [`src/chapters/inform.tex`](src/chapters/inform.tex) | | 🧑‍🎓 |
| A5.3 | "Allfällige Schnittstellen sind ihm im Detail bekannt" | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | 🧑‍🎓 |
| A5.4 | "Allfällige Schnittstellen sind [..] dokumentiert." | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | 🧑‍🎓 |

#### <span id="a6">A6</span>: Testkonzept

| ID    | Anforderung | Referenz | Bemerkungen | Status |
| ----- | ----------- | -------- | ----------- | ------ |
| A6.1a | "Das Testkonzept beschreibt das zu testende System" | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | ⏳ |
| A6.1b | "Das Testkonzept beschreibt [.. die]  Umgebung [des Systems]." | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | ⏳ |
| A6.2 | "Das Testkonzept beschreibt die relevanten Testfälle inkl. der zu erwartenden Ergebnisse." | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | ⏳ |
| A6.3 | "Das Testkonzept begründet nachvollziehbar, was bewusst nicht getestet wird." | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | ⏳ |
| A6.4 | "Das Testkonzept beschreibt die relevanten Testmittel (Hardware, Netzwerk etc.)" | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | ⏳ |
| A6.5 | "Das Testkonzept beschreibt die verwendete(n) Testmethode(n)." | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | ⏳ |

#### <span id="a7">A7</span>: Leistungsfähigkeit

| ID    | Anforderung | Referenz | Bemerkungen | Status |
| ----- | ----------- | -------- | ----------- | ------ |
| A7.1 | "Der Kandidat arbeitete durchwegs engagiert; es gab keine Zeichen von Gleichgültigkeit." | [`src/chapters/journal.tex`](src/chapters/journal.tex) | | ❌ |
| A7.2 | "Der Kandidat geriet nicht in Stresssituationen oder konnte mit diesen souverän umgehen." | [`src/chapters/journal.tex`](src/chapters/journal.tex) | | ❌ |
| A7.3 | "Der Kandidat arbeitete zielorientiert." | [`src/chapters/journal.tex`](src/chapters/journal.tex) | | ❌ |
| A7.4 | "Der Kandidat berücksichtigte die zeitlichen Vorgaben" | [`src/chapters/timeplan.tex`](src/chapters/timeplan.tex) | | ❌ |
| A7.5 | "Der Kandidat dachte über die Aufgabenstellung hinaus und ergänzte nach Möglichkeit eigenständig fehlende Elemente." | [`src/chapters/plan.tex`](src/chapters/plan.tex) | | 🧑‍🎓 |


### Teil B
 - B1: Kurzfassung des IPA-Berichtes
 - B2: Führung des Arbeitsjournals
 - B3: Reflexionsfähigkeit
 - B4: Gliederung
 - B5: Prägnanz
 - [B6: Formale Vollständigkeit des IPA-Berichts](#b6)
 - B7: Sprachlicher Ausdruck und Stil / Rechtschreibung und Grammatik
 - B8: Darstellung
 - B9: Grafiken, Bilder, Diagramme und Tabellen
 - B10: Durchführung und Auswertung der Tests

#### <span id="b6">B6</span>: Formale Vollständigkeit des IPA-Berichts

| ID    | Anforderung | Referenz | Bemerkungen | Status |
| ----- | ----------- | -------- | ----------- | ------ |
| B6.1a | "Der IPA-Bericht ist in Teil 1 (obligatorische Kapitel) und Teil 2(Projekt-Dokumentation) unterteilt." | [`src/index.tex`](src/index.tex) | Die Dokumentation wird in `Umfeld und Ablauf` und `Projekt` aufgeteilt. | ✔️ |
| B6.1b | "Ein allfälliger Quellcode ist im Anhang vorhanden" | [`src/appendix/source.tex`](src/appendix/source.tex) | | ✔️ |
| B6.2a | "Teil 1 enthält: Projektaufbauorganisation" | [`src/chapters/organisation.tex`](src/chapters/organisation.tex) | | ✔️ |
| B6.2b | "Teil 1 enthält: [..] Zeitplan" | [`src/chapters/timeplan.tex`](src/chapters/timeplan.tex) | | ⏳ |
| B6.2c | "Teil 1 enthält: [..] Arbeitsjournal" | [`src/chapters/journal.tex`](src/chapters/journal.tex) | | ⏳ |
| B6.3a | "Der IPA-Bericht enthält ein aktuelles Inhaltsverzeichnis" | [`src/index.tex`](src/index.tex) | Das Inhaltsverzeichnis wird beim Erstellen des Dokuments generiert. | ✔️ |
| B6.4a | "..zu sämtlichen Quellen besteht ein schriftlicher Nachweis" | [`src/index.tex`](src/index.tex) | | ⏳ |
| B6.4b | "die referenzierten Quellen sind gültig und verlässlich;" | [`src/sources.bib`](src/sources.bib) | | 🧑‍🎓 |
| B6.5a | "..auf allen Seiten (optional Titelblatt) eine Kopf- oder Fusszeile mit dem aktuellen Druckdatum und dem Namen des Kandidaten;" | [`src/index.tex`](src/index.tex) |  | ✔️ |
| B6.6a | "...ein alphabetisch sortiertes Glossar mit korrekten Erläuterungen der verwendeten Fachbegriffe und Abkürzungen, welche einer aussenstehenden Fachperson unbekannt sein dürften." | [`src/glossaries.tex`](src/glossaries.tex) | Das Glossar wird automatisch mit den benutzten Einträgen alphabetisch erstellt. Ein Glossareintrag kann mit `\gls{Eintragsname}` benutzt werden. | ✔️ |

## Referenzen

[1]: https://pk19.ch/wp-content/uploads/2021/11/Kriterienkatalog-Standardkriterien_2022.pdf
[2]: https://pk19.ch/wp-content/uploads/2021/11/QV-Leitfaden_2022.pdf