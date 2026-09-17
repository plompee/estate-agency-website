# Estate Agency Website — Apex27 Portal API
> 🚀 **Try it live: [open the working demo](https://plompee.github.io/projects/estate-agency/)** — no setup, runs entirely in your browser.>
A complete estate agency website that runs **100% in the browser** — no backend.

Hartley & Grove is a fictional agency. All property data is a snapshot of the **Apex27 Portal API** (78 listings with full property details, images, floorplans and EPCs). Search, filtering, sorting, pagination and rendering all run client-side in `js/agency.js`.

## Pages

| Page | What it does |
|------|--------------|
| `index.html` | Hero search, featured properties, agency stats |
| `listings.html` | Filter sidebar (transaction type, property type, city, price, beds), sorting, pagination |
| `property.html` | Full detail page via `?id=`: gallery, specs, rooms, floorplans/EPC, enquiry form |
| `valuation.html` | Valuation request form (demo mode) |
| `contact.html` | Contact form (demo mode) |

## Run it

```
python3 -m http.server 8000
# open http://127.0.0.1:8000
```

## Live demo

https://plompee.github.io/projects/estate-agency/

## About the data

`data.js` is a one-time snapshot of the Apex27 Portal API (endpoints: `get-search-options`, `get-listings`, `get-listing`, `get-statistics`). GitHub Pages can't run a backend and the API is not CORS-open to arbitrary origins, so the site ships with the data embedded. To refresh it, re-fetch from the API and regenerate `data.js` in the same shape:

```js
window.AGENCY_DATA = { options, stats, searchIndex, listings }
```

Forms are illustrative — they show a "demo mode" notice instead of submitting.
