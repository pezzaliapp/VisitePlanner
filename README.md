# VisitePlanner — PezzaliAPP

PWA offline per pianificare visite clienti a partire dal **calendario Outlook (CSV)**, con **anagrafica clienti**, suggerimenti automatici e **export .ICS** per re-importare gli appuntamenti in Outlook/Google.
- Import CSV calendario Outlook
- Registro clienti (import/export CSV)
- Calcolo disponibilità per giornata (8h) e **slot visita ≈ 2h**
- Evidenza clienti **URGENTI / PROSSIMI** in base alla frequenza
- Generazione suggerimenti e **export .ICS**
- **Offline** (Service Worker) e dati in **LocalStorage**
- Installabile come app (manifest)

## Deploy rapido
1. Metti la cartella su un hosting statico (GitHub Pages, Netlify, ecc.).
2. Apri `index.html` da browser e **installa** la PWA.
3. Importa CSV di Outlook, aggiungi/Importa i clienti e genera il piano.

## Note CSV Outlook
Colonne attese: `Oggetto, Data inizio, Ora inizio, Data fine, Ora fine, Luogo, Giornata intera`.

## Limitazioni MVP
- Matching cliente ↔ evento basato su **substring** nel titolo.
- Nessun geocoding/tempi di viaggio (si può integrare).
- Orari standard per export: **09:00, 11:30, 14:00, 16:30**.

## Roadmap
- Geocoding + km/tempi (OSM/Google)
- Clustering aree e ordina-percorso
- Sincronizzazione diretta con Outlook/Google via API (OAuth)
