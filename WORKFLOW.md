# WORKFLOW — so geht es in den Folge-Sessions weiter

Dieses Dokument ist so geschrieben, dass eine neue Session (auch nach Wochen) sofort
weiterarbeiten kann. **Immer zuerst [`prospects/index.md`](prospects/index.md) öffnen** und die
nächste Firma mit Status `offen` nehmen.

## Pro Firma: 4 Schritte

### Schritt 1 — Website-Status kurz verifizieren (Pflicht!)
Bevor du eine Seite baust, prüfe per Websuche „<Firmenname> <Ort> website", ob die Firma
inzwischen doch eine gute eigene Website hat.
- Nur Facebook/Instagram/Verzeichnis/TripAdvisor → **guter Zielkunde, weiter mit Schritt 2**.
- Eigene, moderne Website vorhanden → in `index.md` auf `übersprungen` setzen (kurze Notiz warum)
  und die **nächste** Firma nehmen.

### Schritt 2 — Website bauen
- Lies das Profil `prospects/NN-<slug>.md` gründlich (Angebot, Vibe, Farben, Website-Brief).
- Baue eine **eigenständige, responsive** Seite: `sites/<slug>/index.html`
  (alles inline/selbst-enthalten: CSS im `<style>`, keine externen Abhängigkeiten, damit sie
  überall und offline lädt; Bilder als Platzhalter/CSS oder frei lizenzierte Assets, keine
  fremden Logos/urheberrechtlich geschützten Fotos ohne Quelle).
- **Sprache:** in der Landessprache der Firma (im Profil vermerkt), ggf. + Englisch für Touristen.
- Inhalt: nur was du aus dem Profil/öffentlichen Quellen weißt; **nichts erfinden**, was die Firma
  blamieren könnte (keine Fake-Preise, keine erfundenen Auszeichnungen). Platzhalter klar als solche
  kennzeichnen, wo Infos fehlen (z. B. „[Öffnungszeiten bitte ergänzen]").
- Qualität: sauberes, modernes Frontend (klare Typografie, gute Kontraste, Hero + Sektionen,
  mobil zuerst). Design-Skill zeigen — das ist das Verkaufsargument.

### Schritt 3 — Hosten (GitHub Pages)
- Einmalig: GitHub Pages im Repo aktivieren (Settings → Pages → Branch `main` bzw. Arbeitsbranch,
  Ordner `/root`). Danach ist jede Seite live unter
  `https://<github-name>.github.io/<repo>/sites/<slug>/`.
- Live-URL im Browser prüfen (lädt? mobil ok? Links/CTA funktionieren?).
- Live-URL in `prospects/index.md` eintragen.

### Schritt 4 — E-Mail-Entwurf
- Lege `emails/<slug>.md` an: Betreff + Text **in der Landessprache**.
- Aufbau: kurze persönliche Ansprache (nutze die „Personalisierungs-Haken" aus dem Profil) →
  „Ich habe euch eine Website gebaut, hier ist sie: <Live-URL>" → ein klarer, weicher CTA
  („Wenn es euch gefällt, antwortet einfach — wenn nicht, ignoriert die Mail gern").
- **Absenderidentität + Opt-out-Satz** immer rein (rechtlich sauberer, wirkt seriöser).
- Kontaktadresse aus dem Profil übernehmen und mit `(zu prüfen)` markieren — Robin verifiziert
  vor dem Senden.
- Nicht senden — nur Entwurf. Robin reviewt und verschickt selbst.

### Abschluss pro Firma
- `prospects/index.md` aktualisieren (Status → `bereit`, Live-URL + Mail-Pfad eintragen).
- Committen + pushen: `git push -u origin <branch>` (bei Netzfehlern bis zu 4× mit Backoff).

## Reihenfolge / Tempo
Eine Firma nach der anderen. Lieber **eine sehr gute** Seite als fünf mittelmäßige — die Qualität
der Seite ist das ganze Verkaufsargument. Bei Unsicherheiten (Design-Richtung, fehlende Infos)
lieber eine kurze Rückfrage an Robin als raten.

## Definition of Done (gesamtes Projekt)
Alle 20 Firmen: verifiziert → Website live → Mail-Entwurf bereit → in `index.md` als `bereit` markiert.
