# Canimal Spec v0.1

Stand: 2026-10-04

## Idee

Du trackst Essen, Protein und Sport. Dein Tier (z.B. ein Dino) lebt davon: trackst du gut, wird es stark und baut mit dir Muskeln auf. Trackst du lange nichts, wird es schwächer, und die App ruft dich an und fragt, was du gegessen hast.

## MVP (v1)

v1 hat 5 Teile, nicht mehr. Ziel: bauen, nicht weiter planen.

1. **Onboarding:** Gewicht, Größe, Ziel. Daraus Kalorien- und Proteinziel pro Tag.
2. **Tier wählen:** 3 süße Spezialtiere zum Start, z.B. Dino, Drache, eins mehr.
3. **Essen tracken:** Foto vom Essen, KI schätzt Kalorien und Protein, du korrigierst vor dem Speichern. Daneben manuelle Eingabe.
4. **Sport:** Schritte automatisch vom Handy (Apple Health / Health Connect). Dazu ein Wochenplan (welcher Tag, welche Sportart) und ein Haken "war beim Sport".
5. **Erinnerung per Anruf:** Abends ein Anruf (wie Call Frank). Du erzählst, was du gegessen hast, die App trägt es automatisch ein. Plus Push-Notification, wenn lange nichts getrackt wurde.

## Tier-Logik

Das Tier hat einen Zustand, berechnet aus den letzten 24 h und der Woche.

| Zustand | Wann | Was du siehst |
| --- | --- | --- |
| Stark | Proteinziel erreicht + Sport laut Wochenplan | Tier wächst, Muskeln sichtbar |
| Normal | Getrackt, Ziel nicht ganz erreicht | Tier ist fröhlich |
| Müde | Länger nichts getrackt | Tier ist schwächer, schläft viel |

Das Tier verhungert nie und leidet nie unter wenig Essen. Bestraft wird nur Nicht-Tracken, nie eine Diät.

## Später, nicht in v1

- SMS-Erinnerungen
- Mehr Tiere und Tier-Zubehör
- Tagebuch-Frage im Anruf ("Was willst du von heute behalten?")
- Freunde und Tiere vergleichen

## Offene Fragen

- [ ] Ab wie vielen Stunden ohne Tracking kommt der Anruf? Vorschlag: täglich 20 Uhr, nur wenn noch Lücken sind.
- [ ] iOS zuerst oder beide? Vorschlag: Expo, beide gleichzeitig.
- [ ] Welches drittes Tier?
