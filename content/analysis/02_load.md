---
Title: Load
Description: This is our load page.
---

Analys av webbsidors laddningstid och användbarhet
=======================

Jag har valt ut tre olika webbsidor och testat dem för att mäta deras laddningstid och för att se över ifall de kan förbättras på något sätt för att uppnå bättre resultat.
<br><br>
Urval
-----------------------

Jag har valt att undersöka följande webbsidor:
- [Tibia](https://www.tibia.com/news/?subtopic=latestnews)
- [Abaldar](https://abaldar.archlightonline.com/)
- [World of Warcraft](https://worldofwarcraft.blizzard.com/en-gb/)

Detta är tre olika spelsidor. Tibia är ett 25 år gammalt spel med väldigt få användare, med dagens mått mätt. Abaldar är en inofficiell Tibia-server som ägs av en privatperson och World of Warcraft är ett av världens mest populära MMORPG's genom tiderna. Jag valde att undersöka dessa sidorna eftersom det kan vara intressant att se skillnaden mellan ett av världens största spel och ett avsevärt mindre spel, men även en inofficiell version av det.
<br><br>

Metod
-----------------------

Jag använder mig utav [PageSpeed Insights](https://pagespeed.web.dev/) för att mäta performance, accessibility, best practices och SEO (Search Engine Optimization).
<br>
Laddningstid, antal resurser och sidans totala storlek tar jag fram med hjälp av Devtools i Mozilla Firefox.
<br>
Denna gången ville jag testa att ta screenshots på de fullständiga sidorna och inte bara delar av dem, så jag använde mig utav [Nimbus Screenshots](https://nimbusweb.me/screenshot) för att uppnå mitt önskade resultat.
<br><br>

Resultat
-----------------------

**Bilder**

Tryck för att se mer:
<div class="image-container">
<a href="%base_url%/image/tibia.png" target="_blank" rel="noopener noreferrer">
<picture>
    <source media="(min-width: 768px)" srcset="%base_url%/image/tibia.png?w=1072&h=800">
    <img src="%base_url%/image/tibia.png?w=768" alt="tibia">
</picture>
</a>
<a href="%base_url%/image/wow.png" target="_blank" rel="noopener noreferrer">
<picture>
    <source media="(min-width: 768px)" srcset="%base_url%/image/wow.png?w=1072&h=800">
    <img src="%base_url%/image/wow.png?w=768" alt="wow">
</picture>
</a>
<a href="%base_url%/image/abaldar.png" target="_blank" rel="noopener noreferrer">
<picture>
    <source media="(min-width: 768px)" srcset="%base_url%/image/abaldar.png?w=1072&h=800">
    <img src="%base_url%/image/abaldar.png?w=768" alt="abaldar">
</picture>
</a>
</div>
<br><br>
**Mätningar**
<iframe class="load-sheet" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vQYMG_OoJ9OOerY1uy5QW2FoOOBSulJWhaGbUltgdMmpyZulAzqD1ghcYkUjZMj6X_BdAMIFCEjQjYq/pubhtml?gid=0&amp;single=true&amp;widget=true&amp;headers=false"></iframe>
<br><br>
Mina resultat är helt tvärtemot min förväntning. Jag trodde att World of Warcraft skulle ha betydligt högre betyg och laddningstid än de andra sidorna, eftersom budgeten är otroligt mycket större. Deras förstasida hade en laddningstid på 2.37 sekunder, vilket jag ändå anser är okej. Allt under 3 sekunder skulle jag klassifiera som "snabbt". Deras sida är ju däremot mer krävande per definition då de har lite mer komplicerade funktionaliteter. En animerad video som bakgrund, massor med olika bilder, redirects till diverse sidor osv. Jag är chockad över deras dåliga betyg från Google Pagespeed däremot. Desktop-betyget ligger på 30 för förstasidan och Mobile-betyget blev 38. Detta känns ju otroligt dåligt för en sida med så stor användarbas.

**Förbättringar för World of Warcraft:**
- Minska på oanvänd JavaScript. De har mycket JavaScript som laddas in, trots att det inte alltid behövs.
- Hantera bilder på ett modernare sätt. Bildformat som WebP och AVIF ger ofta bättre resultat än JPG och PNG, vilket skulle resultera i snabbare laddningstid.
- Minska på oanvänd CSS. Ta bort oanvända regler från deras stylesheets för att minska på "bytes" som används av nätverket.
<br><br>

Jag blev positivt överraskad över Tibias resultat. Otroligt bra resultat från Google Pagespeed på 95 i Desktop-betyg och runt 70 på Mobile. Sidan har även ypperligt bra laddningstid på under 2 sekunder. Jämför man med World of Warcraft-sidan så ser man ju rätt tydligt att Tibia har en mycket enklare hemsida med mindre funktionaliteter.  

**Förbättringar för Tibia:**
- Hantera bilder på ett modernare sätt. WebP och AVIF ger bättre resultat än JPG och PNG.
- Minska användningen av oanvänd JavaScript.
- Sätta en bestämd height/width på bilder för att minska dess storlek.
<br><br>

Abaldar som är en inofficiell version av Tibia fick ett resultat som mätte mina förväntningar. Det är en inofficiell sida med extremt begränsad budget, vilket förmodligen har resulterat i en sämre hemsida, vilket är förståeligt. Hemsidan fick ett snittbetyg i Desktop på runt 50 och lite bättre för Mobile. Däremot har sidan extremt snabb laddningstid. Detta beror på att den inte har jättemånga resurser att ladda in, eftersom det är en ganska liten webbsida. 

**Förbättringar för Abaldar:**
- Hantera bilder med WebP och AVIF istället för JPG och PNG.
- Ändra bildstorlek ordentligt för att spara otroligt mycket på nätverket.
- Ändra vissa eventlyssnare för beröring- och skrollhändelser till passive för att förbättra prestandan.
<br><br>

Analys
-----------------------

Sammanfattningsvis så ser man ju att alla sidor bör tänka om när det gäller bild-format och användningen av oanvänd JavaScript. Det tar rätt mycket på nätverket att inkludera JavaScript-kod som inte används eller behövs för att rendera eller interagera med sidan, vilket resulterar i onödigt ökad sidstorlek och onödig belastning för webbläsaren. Genom att minska mängden onödig JavaScript och fördröja laddningen av skript som inte behövs omedelbart kan sidans storlek och belastningstid minskas, vilket leder till snabbare laddningstider och en mer responsiv upplevelse för användaren. 
<br><br>

Rangordning
-----------------------
**Förväntat rangordning:**
1. World of Warcraft
2. Tibia
3. Abaldar

**Resulterande rangordning:**
1. Tibia
2. Abaldar
3. World of Warcraft

När det gäller just laddningstid så är det väl rätt förståeligt att World of Warcraft hamnar sist, då de har tyngre resurser att ladda in än de andra två. Däremot är jag chockad över deras låga resultat i Google PageSpeed. Det hade varit intressant att veta ifall de är medvetna om deras resultat och om de planerar att göra någonting åt saken. Jag tror att hade de fått upp sina resultat till Tibias nivå så hade användarupplevelsen blivit bättre.
<br><br>


Gräns för laddningstid
-----------------------
Min personliga gräns skulle jag nog vilja ha under 5 sekunder. Allt över 5 sekunder anser jag vara otroligt slött. Eftersom samtliga av mina urval har en laddningstid på runt 2 sekunder så är de ju otroligt snabba, enligt mig. Jag testade runt lite utav ren nyfikenhet på sidorna som jag undersökte under Färg-analysen; Facebook, Twitter och Instagram. De hade ungefär en hel sekund längre laddningstid, men det är ändå snabbt skulle jag vilja säga. 

<br><br>

Referenser
-----------------------

[PageSpeed Insights](https://pagespeed.web.dev/)

[Nimbus Screenshots](https://nimbusweb.me/screenshot)
<br><br>

Övrigt
-----------------------

Denna rapport är skriven utav Linus Sandin.