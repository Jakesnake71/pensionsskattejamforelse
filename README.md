# Pensionsskattejämförelse

Ett enkelt beslutsstöd som jämför nettoutfallet av pension om den tas ut i Sverige jämfört med andra länder vid utflyttning. Prototyp, inte skatterådgivning.

Appen är en enda statisk HTML-fil (`index.html`) utan byggsteg eller beroenden.

## Kör lokalt

Öppna `index.html` i en webbläsare. Inget mer behövs.

## Publicera på GitHub

1. Skapa ett nytt repo på GitHub, till exempel `pensionsskattejamforelse`.
2. Lägg upp innehållet i den här mappen i repot:

   ```bash
   cd pensionsapp
   git init
   git add .
   git commit -m "Första versionen av pensionsskattejämförelse"
   git branch -M main
   git remote add origin https://github.com/DITT-KONTO/pensionsskattejamforelse.git
   git push -u origin main
   ```

## Publicera på Render

Alternativ A, via blueprint (`render.yaml` finns med i repot):

1. Logga in på render.com och välj New, sedan Blueprint.
2. Anslut ditt GitHub-repo. Render läser `render.yaml` och skapar en statisk sajt automatiskt.
3. Klicka Apply. Efter någon minut får du en publik URL.

Alternativ B, manuellt:

1. New, sedan Static Site.
2. Anslut repot.
3. Build Command lämnas tomt, Publish Directory sätts till `.`
4. Create Static Site.

## Innehåll

- `index.html` – hela appen (inmatning, beräkning, resultat).
- `render.yaml` – blueprint för statisk sajt på Render.

## Att göra i kommande versioner

- Föra in skatteavtalens fördelning per pensionstyp i beräkningen.
- Verifiera skatteskalor och valutakurser mot officiella källor.
- Återinföra grafen över netto per månad och uttagsperiod.
