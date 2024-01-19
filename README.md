# Moment 1, automatisering och publicering
Momentet syftar till att ge mig en grund för hur NodeJS och NPM kan underlätta mitt arbete med webbplatsutveckling.
Grunden handlar om att med hjälp av NPM och PARCEL skapa en automatiserad utvecklingsmiljö och publiceringsmetod.
Detta optimerar och minifiera olika filer och publicerar även projektändringar direkt utan någon manuell push.

## Uppgiftens olika steg

1. Skapa ett nytt NPM-projekt med *npm init* i terminalen. En package.json-fil med information om projektet skapas.
2. Installera PARCEL-paketet med *npm install parcel --save-dev*. Detta installerar paketet som ett utvecklingsberoende och mappen node_modules skapas. 
3. Skapa en .gitignore-fil där node_modules/ skrivs in. Detta gör att mappen inte versionhanteras.
4. Ange i informationen (package.json) vilken startfil projektet ska ha; .index.html anges.
5. Skapa katalog med namnet src. Här samlas alla projekt-filer som är under utveckling.
6. Lägg till scripts i informationen (package.json). Ange "parcel" som start och "parcel build" som build. Detta paketerar ihop webbplatsen olika delar inför publicering.
7. Ange type="module" inom script-taggen i HTML-filerna. PARCEL paketerar då ihop samtliga JS-filer i en extern fil automatiskt vid publicering.
8. Testkör projektet genom *npm start* i terminalen. PARCEL startas och skapar en live-server där webbplatsen visas. Filerna för visning/testkörning läggs i en ny .dist-mapp medan src-mappen förblir en mapp för arbetsfiler.
9. Kör *npm run build* i terminalen för att publicera webbplatsen. Det som sker automatiskt är att HTML-filerna och CSS-filerna samt minifierar och transpilerar JS-filerna.
10.  
