# Family UNO

Private 2–4 player UNO frontend.

Backend: Supabase Edge Function `uno-api-v2`.

## Local testing

Serve this folder over HTTP; do not open `index.html` directly:

```powershell
cd familyuno
py -m http.server 5500
```

Open `http://localhost:5500`. The deployed Supabase function is used by default.
To test another function endpoint, pass it as the `api` query parameter:

```text
http://localhost:5500/?api=http%3A%2F%2F127.0.0.1%3A54321%2Ffunctions%2Fv1%2Funo-api-v2
```

Use two browser windows, or one normal window and one private window, to test two players. Clear the site's local storage between unrelated games.

## Hosting
Upload `index.html` to any static host (Vercel, Netlify, GitHub Pages, etc.).
No build step is required.

## Important
The backend keeps hands in a private table and exposes only the current player's hand.
