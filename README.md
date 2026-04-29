# Iconic Live Couture – Webshop

## Deployment auf Vercel

### Schritt 1: GitHub Repository erstellen
1. github.com → "New repository"
2. Name: `ilc-shop`
3. Alle Dateien aus diesem ZIP hochladen

### Schritt 2: Vercel verbinden
1. vercel.com → "Add New Project"
2. GitHub-Repo `ilc-shop` auswählen → "Import"
3. Framework: **Other** (kein Framework)
4. Deploy klicken

### Schritt 3: Environment Variables setzen
In Vercel → Project Settings → Environment Variables:

| Name | Value |
|------|-------|
| `STRIPE_SECRET_KEY` | sk_test_51TRaSC... (dein Secret Key) |
| `NEXT_PUBLIC_SITE_URL` | https://deine-domain.vercel.app |

### Schritt 4: Redeploy
Nach dem Setzen der Env Vars → Deployments → "Redeploy"

### Schritt 5: Live gehen
- Stripe Dashboard → Testmodus ausschalten → Live-Keys eintragen
- Fertig! 🎉

## Dateistruktur
```
/
├── index.html          ← Dein Shop
├── success.html        ← Erfolgsseite nach Kauf
├── package.json        ← Node Dependencies
├── vercel.json         ← Vercel Konfiguration
└── api/
    └── checkout.js     ← Stripe Serverless Function
```

## Test-Kreditkarte (Stripe Testmodus)
- Nummer: 4242 4242 4242 4242
- Datum: beliebig in der Zukunft
- CVV: beliebig
