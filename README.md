# Phishing-demo (sikkerhetsforedrag)

En **pedagogisk** phishing-demo for Bredvid. Siden etterligner Microsoft/Entra SSO-innloggingen.
Publikum skanner en QR-kode, skriver inn jobb-e-posten, og i stedet for passord får de
en «du ble phishet»-side med en fisker. 🎣

## Viktig: etisk ramme
- **Ingenting lagres eller sendes.** E-posten forlater aldri nettleseren – den brukes kun
  til å utløse avsløringssiden, så kastes den. Ingen backend, ingen logging, ingen tracking.
- **Ingen passordfelt.** Demoen samler aldri inn legitimasjon.
- Ment for ditt eget, samtykkende publikum. **Ta siden ned etter foredraget** – en lookalike
  Microsoft-innlogging bør ikke ligge offentlig over tid.

## Filer
- `index.html` – alt i én fil (innlogging + avsløring).
- `bredvid-logo.svg` – logo (hentet fra hvaskjer-repoet).

## Kjøre lokalt
Åpne `index.html` i en nettleser, eller start en enkel server:

```bash
cd qr-ai-code && python3 -m http.server 8000
```

Så: http://localhost:8000

## Deploye raskt (for QR-kode)
Statisk side – deploy hvor som helst. F.eks.:

```bash
cd qr-ai-code && npx vercel --prod
```

Lag deretter en QR-kode som peker på URL-en. Bruk gjerne et nøytralt domene du
kontrollerer (ikke et som faktisk utgir seg for å være microsoft.com).
