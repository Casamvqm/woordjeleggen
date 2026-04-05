# Wordfeud NL 🎲

Een volledig speelbare Nederlandse versie van Wordfeud (Scrabble-achtig woordspel) als single-page webapplicatie.

## Functies

- **15×15 bord** met standaard Wordfeud bonusvakjes (dubbele/drievoudige letter en woord)
- **Nederlandse letters** met correcte verdeling en puntwaarden
- **Woordvalidatie** via de OpenTaal woordenlijst (automatisch geladen)
- **Twee spelers** op één apparaat (hot-seat modus)
- **Jokers** — kies zelf welke letter een blanco tegel voorstelt
- **Bingo bonus** (+50 punten) bij gebruik van alle 7 letters
- **Letters ruilen** en beurt passen
- **Automatische eindgamedetectie**
- **Responsive** — speelbaar op desktop en tablet

## Puntwaarden (Nederlands)

| Letter | Punten | Aantal |
|--------|--------|--------|
| E, N, A, O, I, D, R, S, T | 1–2 | veel |
| G, K, L, M, B, P | 3 | normaal |
| H, U, V, F, J | 4 | weinig |
| Z, C, W | 4–5 | weinig |
| X, Y, Q | 8–10 | 1 |
| * (joker) | 0 | 2 |

## Installatie

```bash
# 1. Clone de repository
git clone https://github.com/jouw-naam/wordfeud-nl.git
cd wordfeud-nl

# 2. Installeer afhankelijkheden
npm install

# 3. Start de ontwikkelserver
npm run dev
```

Open vervolgens [http://localhost:3000](http://localhost:3000) in je browser.

## Bouwen voor productie

```bash
npm run build
```

De gebouwde bestanden staan in de `dist/` map.

## Deployen op Vercel

1. Push de code naar GitHub
2. Ga naar [vercel.com](https://vercel.com) en importeer het repository
3. Vercel detecteert Vite automatisch — klik op **Deploy**

Of gebruik de Vercel CLI:

```bash
npm i -g vercel
vercel
```

## Spelregels

1. **Eerste zet**: moet het middelste vakje (★) bedekken, minimaal 2 letters
2. **Vervolg**: nieuwe letters moeten aansluiten op bestaande woorden
3. **Richting**: alle letters van één zet moeten in dezelfde rij of kolom liggen
4. **Woorden**: alle gevormde woorden (horizontaal én verticaal) moeten geldig zijn
5. **Bonusvakjes**: tellen alleen mee bij de eerste keer dat ze bedekt worden
6. **Bingo**: gebruik je alle 7 letters, dan krijg je +50 extra punten
7. **Einde**: het spel eindigt als de zak leeg is en een speler geen letters meer heeft, of als beide spelers twee keer achter elkaar passen

## Tech stack

- **React 18** met hooks
- **Vite** als build tool
- **CSS Modules** voor styling
- **OpenTaal** woordenlijst voor validatie
- Geen backend — alles draait client-side

## Licentie

MIT
