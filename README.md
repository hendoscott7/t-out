# T-Out

Days out for Theo. A map of places around Belfast for a toddler, with one tap to pick somewhere that suits today.

Live: https://hendoscott7.github.io/t-out/

## Using it

- **The sentence** sets the filters: *"It's dry, run him ragged, free, under 30 min, every kind."* Tap any underlined phrase to cycle through its options. Grey means "any".
  - **Weather:** rain or shine / it's dry / it's raining. Each day it starts on Belfast's forecast.
  - **Mood:** any mood / run him ragged / keep it calm.
  - **Price:** any price / free / cheap.
  - **Distance:** any distance / under 15 min / under 30 min / under an hour.
  - **Kind:** every kind, or one kind in its own colour (outdoors, animals, museums, groups, other). This is also the colour key for the map dots, and the coloured tag on each place. Soft play isn't a category; any soft play on your own list sits under other, with markets.
- **The map** shows every place as a dot in its kind's colour. Places that don't fit the sentence fade out, and hollow dots are places you've been. Drag, pinch and tap as normal. The ⓘ shows the map credits.
- **The shelf** at the bottom says "Where to?". Pull it up and it picks somewhere, favouring places you haven't been and avoiding recent picks. The map flies to the pick.
  - The open shelf shows the kind, inside/outside, cost and drive time, a note, recent photos taken near the place (Wikimedia Commons, 2018 on), and **Directions** to Google Maps.
  - The round button top right picks another. Pull the shelf down to tuck it away.
  - Tap the place's name to fix its tags, add a note, log a visit or remove it.
- **Weather and temperature** top right come from Open-Meteo, a free forecast service that needs no key.

Follows the phone's light or dark mode. Everything you change is saved in the browser (`localStorage`).

## Editing the places

Everything is in `index.html`:

- `IDEAS` lists each place: `[id, name, area, kind, inside/outside/both, cost 0–2, minutes from Belfast, mood, note]`.
- `AT` gives each place's `[lat, lng]`. These are approximate.
- Kinds and their colours: outdoors (park, woods, beach) green, animals rust, museums and space indigo, groups and markets ochre, other grey (`--h0`…`--h5` in the CSS).

New ideas appear for existing users on their next visit. Ones they've removed don't come back.

## Credits

Map tiles: Esri (World Light/Dark Gray Canvas). Outline map: Natural Earth. Map library: Leaflet. Photos: Wikimedia Commons. Weather: Open-Meteo.
