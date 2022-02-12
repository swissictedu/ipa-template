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
| ✔️ | Dieses Kriterium wird in der Vorlage beispielhaft umgesetzt. |
| ⏳ | Dieses Kriterium wird noch nicht in der Vorlage umgesetzt. |
| ❌ | Dieses Kriterium kann nicht in der Vorlage umgesetzt werden. |
| 🧑‍🎓 | Dieses Kriterium muss individuell in der Vorlage geprüft oder umgesetzt werden. |

### Teil A
 - A1: Projektmanagement und Planung
 - A2: Wissensbeschaffung
 - A3: Zeitplan
 - A4: Konzeptionelle Umsetzung
 - A5: Projektumfeld: Systemgrenzen / Schnittstellen zur Aussenwelt
 - A6: Testkonzept
 - A7: Leistungsfähigkeit
 - A8: Selbständiges Arbeiten
 - A9: Fachkenntnisse und Anwendungskompetenz
 - A10: Anwendung der Fachsprache
 - A11: Arbeits- und Fachmethodik
 - A12: Organisation der Arbeitsergebnisse
 - A13: IPA-Erfüllungsgrad

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
| B6.1b | "Ein allfälliger Quellcode ist im Anhang vorhanden" | [`src/appendix/source.tex`](src/appendix/source.tex) |  | ✔️ |
| B6.2a | "Teil 1 enthält: Projektaufbauorganisation" | [`src/chapters/organisation.tex`](src/chapters/organisation.tex) |  | ✔️ |
| B6.2b | "Teil 1 enthält: [..] Zeitplan" | [`src/chapters/timeplan.tex`](src/chapters/timeplan.tex) |  | ⏳ |
| B6.2c | "Teil 1 enthält: [..] Arbeitsjournal" | [`src/chapters/journal.tex`](src/chapters/journal.tex) |  | ⏳ |
| B6.3a | "Der IPA-Bericht enthält ein aktuelles Inhaltsverzeichnis" | [`src/index.tex`](src/index.tex) | Das Inhaltsverzeichnis wird beim Erstellen des Dokuments generiert. | ✔️ |
| B6.4a | "..zu sämtlichen Quellen besteht ein schriftlicher Nachweis" | [`src/index.tex`](src/index.tex) |  | ⏳ |
| B6.4b | "die referenzierten Quellen sind gültig und verlässlich;" | [`src/sources.bib`](src/sources.bib) |  | 🧑‍🎓 |
| B6.5a | "..auf allen Seiten (optional Titelblatt) eine Kopf- oder Fusszeile mit dem aktuellen Druckdatum und dem Namen des Kandidaten;" | [`src/index.tex`](src/index.tex) |  | ✔️ |
| B6.6a | "...ein alphabetisch sortiertes Glossar mit korrekten Erläuterungen der verwendeten Fachbegriffe und Abkürzungen, welche einer aussenstehenden Fachperson unbekannt sein dürften." | [`src/glossaries.tex`](src/glossaries.tex) | Das Glossar wird automatisch mit den benutzten Einträgen alphabetisch erstellt. Ein Glossareintrag kann mit `\gls{Eintragsname}` benutzt werden. | ✔️ |

## Referenzen

[1]: https://pk19.ch/wp-content/uploads/2021/11/Kriterienkatalog-Standardkriterien_2022.pdf
[2]: https://pk19.ch/wp-content/uploads/2021/11/QV-Leitfaden_2022.pdf