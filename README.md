# 🐾 Stray

**Una rete di aiuto per gli animali randagi, feriti, malnutriti o maltrattati in tutta Europa.**

Stray è una web-app leggera (solo HTML/CSS/JS, nessun build, nessun backend) pensata
per chiunque si trovi davanti a un animale in difficoltà e non sappia a chi rivolgersi.
Cerca il paese in cui ti trovi, trova i contatti di emergenza locali, segnala l'animale
con foto e posizione e coordinati con i volontari della zona.

## Pagine

| File | Cosa fa |
|------|---------|
| `index.html` | Home: ricerca città/paese, contatti di emergenza, modulo di segnalazione, ultime segnalazioni, menu, info e contatti. |
| `registrati.html` | Registrazione guidata in 4 passi (volontario o associazione) con validazione e indicatore forza password. |
| `segnalazione.html` | Dettaglio di una segnalazione: foto, stato, posizione (visibile ai soli registrati), "Mi occupo io" e discussione con risposte. |
| `account.html` | Profilo utente: statistiche, filtro per paese, le proprie segnalazioni, accesso/uscita. |

## Caratteristiche

- **Facile e fluido**: ricerca immediata, animazioni morbide, design mobile-first.
- **12 paesi europei** con contatti di emergenza reali.
- **Funziona offline**: i dati (segnalazioni, account, commenti) sono salvati in
  `localStorage` del browser — le pagine si scambiano i dati tra loro.
- **Accesso differenziato**: chiunque vede foto e paese; solo i registrati vedono
  indirizzo esatto e contatti e possono intervenire.

## Come provarlo

Apri `index.html` nel browser, oppure servi la cartella:

```bash
npx serve .
```

## Modello dati (localStorage)

- `stray_user` — utente registrato `{nome, email, tipo, paese:{code,name}, avatar}`
- `stray_r` — elenco segnalazioni `[{id, ts, type, needs, desc, location, photo, country, countryName, stato, nomeUtente}]`
- `stray_comments_<id>` — discussione di una segnalazione

---

> *One stray, at a time.* — Stray Project
