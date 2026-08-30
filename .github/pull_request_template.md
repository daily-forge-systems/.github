<!--
Für einen Release-PR (develop -> main) nicht diese Vorlage verwenden, sondern
?template=release.md anhängen - siehe docs/workflows/release.md.

Im Alltag wird in diesem Workspace direkt auf develop committet; ein PR ist die
Ausnahme. Wenn du hier bist, gibt es also einen Grund - nenne ihn.
-->

## Worum geht es?

<!-- Was ändert sich, und warum? Das Was zeigt der Diff; das Warum nicht. -->

Schließt: <!-- #123, oder "kein Issue" mit Begründung -->

## Art der Änderung

<!-- Der Conventional-Commit-Typ, der zum Inhalt passt. Nur einer. -->

- [ ] `feat` — neue Funktion
- [ ] `fix` — Fehlerbehebung
- [ ] `refactor` — Struktur geändert, Verhalten nicht
- [ ] `perf` — Laufzeit oder Ressourcen
- [ ] `docs` — nur Dokumentation
- [ ] `test` — nur Tests
- [ ] `build` / `ci` / `chore` — Werkzeuge, Abhängigkeiten, Infrastruktur
- [ ] Breaking Change — dann mit `!` im Typ und `BREAKING CHANGE:`-Footer

## Wie wurde geprüft?

<!--
Die tatsächlich ausgeführten Befehle und ihre Ausgabe, nicht die Absicht.
Eine Aussage über bestandene Tests ohne ausgeführten Lauf ist unzulässig.
Wurde etwas übersprungen oder ist rot, gehört das hierher - nicht weggelassen.
-->

```

```

## Checkliste

- [ ] Tests für die geänderte Logik geschrieben und ausgeführt; bei einer Fehlerbehebung ein Regressionstest, der den Fehler ohne die Korrektur reproduziert
- [ ] Linter und Formatierer der betroffenen Pakete ohne Befund — auf Paket-, nicht auf Dateiebene ausgeführt
- [ ] Alle Schritte gelaufen, die die CI-Datei des Repos für diese Änderung ausführt (nicht nur die vermuteten)
- [ ] Öffentliche Symbole dokumentiert; Kommentare erklären das Warum, nicht das Was
- [ ] Keine Geheimnisse, Zugangsdaten oder echten Kunden-, Patienten- und Zahlungsdaten in Code, Konfiguration, Logs, Tests oder Commit-Nachricht
- [ ] `compliance/*.json` im selben Vorgang mitgeführt, falls Zweck, Daten, Aufbewahrung, Rechte, Netzwerk, Anbieter, Modelle oder Sicherheitskontrollen berührt sind (`docs/workflows/compliance-change.md`)
- [ ] Bei Änderungen an `forge_common`: Rückwärtskompatibilität geprüft, jede konsumierende App betrachtet (`docs/workflows/forge-common-api-change.md`)
- [ ] Dokumentation und Konventionsdateien nachgezogen, falls sich eine Konvention geändert hat

## Offen geblieben

<!--
Bewusste Auslassungen, bekannte Einschränkungen, Folgearbeit. Lieber hier
benannt als später entdeckt. "Nichts" ist eine gültige Antwort.
-->
