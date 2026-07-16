# Website-Outreach — Spec-Websites als Vertriebskanal

Ein Projekt, um mit dem Bau von Websites Geld zu verdienen — **ohne Cold Calls**.

## Die Idee

Statt Firmen anzufragen, ob sie eine Website wollen, wird die **fertige,
personalisierte Website vorab gebaut** und der Firma per E-Mail geschickt:
„Schau mal, das habe ich für euch gemacht." Die Firma erkundet die Live-Seite und
antwortet. Für den Kunden ist die Hürde minimal — es liegt schon etwas Fertiges vor,
kein abstraktes Angebot.

Zielkunden sind **Betriebe ohne (oder mit sehr schlechter) Website** — vor allem
traditionelle Handwerks- und Familienbetriebe (Töpfereien, Webereien, kleine Tavernen,
Laternen-/Batik-/Schnitzwerkstätten). Diese Betriebe haben oft eine treue Kundschaft und
internationales Interesse, aber keinen Online-Auftritt — genau die Lücke, die wir füllen.

## Ablauf (mehrere Sessions, alles vom Handy)

1. **Session 1 (erledigt):** 20 reale Firmen recherchiert + tiefe Personalisierungs-Profile
   → siehe [`prospects/`](prospects/).
2. **Folge-Sessions:** Pro Firma eine schöne, responsive Website bauen → kostenlos hosten
   (GitHub Pages) → E-Mail-Entwurf in Landessprache. Robin reviewt und **verschickt selbst**.
   → Anleitung in [`WORKFLOW.md`](WORKFLOW.md).

## Ordnerstruktur

```
README.md                 # dieses Dokument
WORKFLOW.md               # Schritt-für-Schritt für Folge-Sessions (resumierbar)
prospects/
  index.md                # Statustabelle aller 20 Firmen
  01-...md ... 20-...md    # 1 Profil pro Firma (tiefe Infos für die Personalisierung)
sites/                    # (Folge-Sessions) fertige Websites, je Firma ein Ordner
  <slug>/index.html
emails/                   # (Folge-Sessions) Mail-Entwürfe je Firma
  <slug>.md
```

## Hosting

**GitHub Pages** (kostenlos) über den Workflow `.github/workflows/pages.yml`.
Veröffentlicht wird **nur der `sites/`-Ordner** (die Kunden-Websites) — `prospects/` und `emails/`
bleiben bewusst **nicht** im Web. Live-URLs:
`https://clappedbytxger.github.io/GitHubTimoRobin/<ordner>/` (z. B. `.../olaria-patalim/`).

**⚠️ Einmalige Einstellung nötig (nur Repo-Besitzer):** Der Actions-Token darf Pages standardmäßig
nicht aktivieren (Fehler „Resource not accessible by integration"). Fix (30 Sek.):
> **Settings → Actions → General → Workflow permissions → „Read and write permissions" → Save.**
Danach den Workflow „Deploy client sites to GitHub Pages" erneut ausführen (Re-run). Ab dann
deployt jeder Push automatisch. Alternativ: **Settings → Pages → Source → „GitHub Actions"**.

Später optional pro Kunde eine eigene Domain für mehr „Wow" — im ersten Durchlauf nicht nötig.

## Wichtige Hinweise (bitte lesen)

- **Kontaktdaten immer verifizieren.** Die in den Profilen genannten E-Mails/Telefonnummern
  stammen aus öffentlicher Recherche und sind mit `(zu prüfen)` markiert. **Vor dem Versand
  jede Adresse selbst bestätigen** (auf der Google-/Facebook-Seite der Firma).
- **Website-Status verifizieren.** Jede Firma wurde als „keine/sehr schlechte Website" recherchiert;
  Betriebe ändern das aber. **Schritt 1 vor dem Bau: kurz prüfen, dass es wirklich noch keine gute
  Seite gibt** (siehe WORKFLOW).
- **Recht (Cold E-Mail).** Unaufgeforderte Werbe-Mails an Firmen sind je nach Land unterschiedlich
  reguliert (in der EU/DE nach §7 UWG restriktiv, in vielen Ländern lockerer). Mails weich halten,
  klare Absenderidentität + ein Satz „Wenn kein Interesse besteht, einfach ignorieren/kurz Bescheid
  geben". Der Versand und die rechtliche Verantwortung liegen bei Robin.
- **Datenaktualität.** Alle Infos sind Recherchestand Juli 2026 und können veraltet sein.

## Status

- [x] 20 Firmenprofile recherchiert (Session 1)
- [x] Websites gebaut: **20 von 20 fertig** (01–20)
- [x] E-Mail-Entwürfe für alle 20 erstellt
- [ ] GitHub Pages aktiviert — Workflow steht, wartet auf einmalige Einstellung (siehe Hosting)
- [ ] E-Mail-Entwürfe erstellt
