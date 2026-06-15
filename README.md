# Governing the poor — A Historical Atlas, c.1471–1905

A StoryMapJS atlas tracing welfare provision in Glasgow across 450 years and four distinct provider types: church/ecclesiastical, civic and trade philanthropy, the statutory Poor Law, and evangelical voluntary organisations.

**42 slides · 4 provider categories · c.1471 to 1905**

---

## View the map

Hosted on GitHub Pages: **[your-username.github.io/your-repo-name]()**

*(Replace with your actual Pages URL after enabling GitHub Pages in repo Settings → Pages → Source: main branch, / (root))*

---

## Provider categories

| Colour | Category | Period(s) |
|---|---|---|
| 🟧 Amber | Church / ecclesiastical | 1471–1597 |
| 🟦 Slate | Civic & trade philanthropy | 1605–1733 |
| 🟥 Red | Statutory Poor Law | 1845–1905 |
| 🟩 Green | Evangelical voluntary | 1815–1905 |
| 🌿 Olive | Emigration infrastructure | 1819–1917 |

---

## Sites covered

### Church / Ecclesiastical
- St Nicholas Hospital, Castle Street (1471)
- Glasgow Cathedral — Kirk Session poor relief (1560–1597)

### Civic & Trade Philanthropy
- Trades Almshouse, High Street / Cathedral Street (c.1605)
- Hutcheson's Hospital, Trongate → Hutchesons' Hall, Ingram Street (1641)
- Town's Hospital and Poorhouse, Great Clyde Street (1733–1844)

### Evangelical Voluntary
- Tron Kirk — Chalmers' ministry (1815–1819)
- St John's Parish — the Chalmers experiment (1819–1823)
- Glasgow City Mission (founded 1826)
- Night Asylum for the Houseless, North Frederick Street (1838)
- Industrial Brigade Home, Trongate (1864) — Quarrier
- Girls Home, 93 Renfield Street (1871) — Quarrier
- Boys and Girls Home (c.1872) — Quarrier
- Orphan Home Mission Hall and Children's Night Refuge, Dovehill (1872) — Quarrier
- Boys Training Home for Canada, Cessnock House, Govan (1872) — Quarrier
- Girls' Training Home for Canada (c.1872) — Quarrier
- City Orphan Home, James Morrison Street (1875) — Quarrier
- Adelaide Place Baptist Church, Bath Street (1875–77)
- Quarrier's Village, Bridge of Weir (1878)
- House of Refuge for Females (Magdalene Institution) (1812–1858)
- Magdalene Institution, Lochburn House, Maryhill (1857–1958)
- Magdalene Institution (Sisters of the Good Shepherd), Parkhead (1850s)
- Home for Deserted Mothers, 140 Rottenrow (pre-1873–1880s)
- Home for Deserted Mothers (later premises, 1880s)
- Girls' Orphanage (shown on 1892 OS map), Govan area

### Statutory Poor Law
- Poor Law Act 1845 — Barony Hall, Castle Street
- Glasgow City Poorhouse, Parliamentary Road / North Hanover Street (1845–1898)
- Barnhill Poorhouse, Springburn (1853–1905+)
- Govan Poorhouse, Eglinton Street (1852)
- Govan Combination Poorhouse (1875)
- Lock Hospital for Women, Rottenrow (1805–1947)
- Corporation Women's Home (c.1880s)
- Stobhill Hospital and Poorhouse, Springburn (1904)
- Asylum for Indigent Old Men and Old Women's Home
- Boys Home, central Glasgow
- Parkhead Reformatory (Boys) (c.1854)

### Emigration Infrastructure
- Allan Line Shipping Offices, 70 Great Clyde Street (1819 onward)
- Allan Line Buildings, 15–25 Bothwell Street (1890s)
- Allan Line Passenger Booking Office, 75 Buchanan Street (1890s)

### Archive
- Heatherbank Museum of Social Work, Bishopbriggs (Glasgow Caledonian University)

---

## Files

| File | Purpose |
|---|---|
| `index.html` | Page template — loads StoryMapJS from Knight Lab CDN, fetches `storymap.json` |
| `storymap.json` | All 42 slides: headlines, narratives, coordinates, image references |
| `README.md` | This file |

The data is kept in `storymap.json` separately from the HTML so slides can be edited without touching the page template. To add, remove or edit a slide, edit `storymap.json` only.

---

## Editing slides

Each slide in `storymap.json` has this structure:

```json
{
  "text": {
    "headline": "1733 — Town's Hospital, Great Clyde Street",
    "text": "<p>Narrative text here. HTML is supported.</p>"
  },
  "media": {
    "url": "https://upload.wikimedia.org/...",
    "credit": "Image credit",
    "caption": "Caption text"
  },
  "location": {
    "lat": 55.8552,
    "lon": -4.2522,
    "zoom": 16,
    "line": true
  }
}
```

**Overview slides** (intro and closing) additionally have `"type": "overview"` and use `"line": false`.

---

## Running locally

GitHub Pages serves the files over HTTP, which is required for the `fetch()` call that loads `storymap.json`. If you want to preview locally before pushing:

```bash
# Python (built-in)
python3 -m http.server 8000
# then open http://localhost:8000

# Node.js
npx serve .
# then open http://localhost:3000
```

Opening `index.html` directly via `file://` will show an error — this is a browser security restriction on local file fetches, not a bug.

---

## Sources

- [Canmore / Historic Environment Scotland](https://canmore.org.uk) — listed building records and site histories
- [workhouses.org.uk](https://www.workhouses.org.uk/Glasgow/) — Peter Higginbotham's Glasgow poorhouse pages
- [TheGlasgowStory](https://www.theglasgowstory.com) — images and narratives from the Heatherbank Museum of Social Work
- [Glasgow and West of Scotland Family History Society](https://www.gwsfhs.org.uk) — Night Asylum and Lock Hospital accounts
- [Heatherbank Museum of Social Work, Glasgow Caledonian University](https://www.gcu.ac.uk/library/heatherbank) — primary archive
- [iriss.org.uk/goldenbridge](https://content.iriss.org.uk/goldenbridge/) — Quarrier's child emigration programme
- [womenshistoryscotland.org](https://womenshistoryscotland.org) — Lock Hospital and Magdalene Institution history
- [glasgowheritage.org.uk](https://www.glasgowheritage.org.uk) — Lock Hospital narrative
- [historic-hospitals.com](https://historic-hospitals.com/gazetteer/glasgow/) — Glasgow hospital gazetteer
- [glasgowpunter.blogspot.com](http://glasgowpunter.blogspot.com/2015/11/the-glasgow-poorhouses.html) — poorhouse histories

Images sourced from [Wikimedia Commons](https://commons.wikimedia.org) under CC-BY-SA licences and the public domain. See individual slide credits.

---

## Built with

- [StoryMapJS](https://storymap.knightlab.com) — Knight Lab, Northwestern University (open source, MPL 2.0)
- [OpenStreetMap](https://www.openstreetmap.org) — base map tiles (ODbL)

---

## Licence

Narrative text and editorial content: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)  
Images: individual licences as credited in each slide  
StoryMapJS library: [MPL 2.0](https://github.com/NUKnightLab/StoryMapJS/blob/master/LICENSE)
