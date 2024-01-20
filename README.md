# Moment 1, automatisering och publicering
Momentet syftar till att ge mig en grund för hur NodeJS och NPM kan underlätta mitt arbete med webbplatsutveckling.
Grunden handlar om att med hjälp av NPM och PARCEL skapa en automatiserad utvecklingsmiljö och publiceringsmetod.
Detta optimerar och minifiera olika filer och publicerar även projektändringar automatiskt.

## Uppgiftens olika steg

1. Skapa ett nytt NPM-projekt med *npm init* i terminalen. En package.json-fil med information om projektet skapas.
2. Installera PARCEL-paketet med *npm install parcel --save-dev*. Detta installerar paketet som ett utvecklingsberoende och mappen node_modules skapas. 
3. Skapa en .gitignore-fil där node_modules/ skrivs in. Detta gör att mappen inte versionhanteras.
4. Ange i informationen (package.json) vilken startfil projektet ska ha; .index.html anges.
5. Skapa katalog med namnet src. Här samlas alla projekt-filer som är under utveckling. Lägg in filer för den redan påbörjade webbplatsen.
6. Lägg till scripts i informationen (package.json). Ange "parcel" som start och "parcel build" som build. Detta paketerar ihop webbplatsens olika delar inför publicering.
7. Ange type="module" inom script-taggen i HTML-filerna. PARCEL paketerar då ihop samtliga JS-filer i en extern fil automatiskt vid publicering.
8. Testkör projektet genom *npm start* i terminalen. PARCEL startas och skapar en live-server där webbplatsen visas. Filerna för visning/testkörning läggs i en ny .dist-mapp medan src-mappen förblir en mapp för arbetsfiler.
9. Kör *npm run build* i terminalen för att göra webbplatsen redo för publicering. Det som sker automatiskt är att HTML-filerna, CSS-filen och JS-filen minifieras. Det transpilerar även JS-filen.
10. Lägg till .dist samt .parcel-cache i .gitignore. De kommer då inte versionhanteras.
11. Skapa en README-fil och publicera projektet till GitHub. Projektet publiceras och en första commit görs automatiskt.
12. Publicera projektet på plattformen Netlify. Bygg-kommandot är npm run build medan publicerings-mapp är .dist.  
13. Skapa en dev-branch i GitHub. Arbetsfiler och publicerings-filer skiljs då åt under utvecklingen av webbplatsen tills dess att den är klar.
14. Möjliggör bakåtkompabilitet genom att lägga till browserslist-inställningar i package.json-filen.
15. Gör en commit med ändringarna för steg 14, denna gång till dev-branchen.
16. Skapa ett innehåll med text på index.html och process.html och gör commits efter varje sida blivit klar.
17. Skapa ett innehåll med bilder på photos.html och nyttja PARCELs stöd för bildhantering genom inställningar i srcset-taggen. Bilderna storleksändras, konverteras och optimeras då enligt inställningarna. Gör en commit med ändringarna.
18. Skapa en sharp.config.json-fil och ange bildinställningar för jpeg-format och webp-format. Gör en commit med ändringarna.
19. Gör en merge av dev-branchen och main-branchen så att samtliga filer och en uppdaterad och klar version av webbplatsen ligger samlad i main.
20. Kör kommandot npm run build i terminalen och publicerar den färdiga webbplatsen på Netlify.