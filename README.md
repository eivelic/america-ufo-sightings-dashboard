# Interaktivna nadzorna ploča za prostorno-vremensku analizu UFO incidenata

Ovaj projekt predstavlja interaktivnu web nadzornu ploču (Dashboard) za vizualizaciju, filtriranje i analizu višedimenzionalnih podataka o neidentificiranim zračnim fenomenima (UFO/NLO) na teritoriju SAD-a kroz razdoblje od 1969. do 2019. godine. 

Aplikacija je u potpunosti izgrađena na klijentskoj strani (Core JS) koristeći biblioteku **D3.js (v3)**, **HTML5**, **CSS3** i **GeoJSON** kartografski model.

## Ključne funkcionalnosti

* **Interaktivna taktička karta (Albers USA projekcija):** Prostorni prikaz lokacija viđenja s ugrađenom animacijom kronološkog razvoja događaja kroz godine (Play/Pause kontrole i vremenski slider).
* **Frekvencijska analiza oblika (Bar Chart):** Dinamički histogram koji prikazuje top 7 najčešćih geometrijskih oblika objekata s mogućnošću filtriranja po svakoj pojedinoj saveznoj državi.
* **Analiza povijesnih trendova (Line Chart):** Linijski grafikon koji prati fluktuaciju prijava kroz desetljeća s interaktivnim filtrom za selekciju specifičnih oblika.
* **Evaluacija korelacije (Scatter Plot):** Dvodimenzionalni graf raspršenja koji analizira utjecaj doba dana (sat u danu) na trajanje fenomena (u sekundama).
* **Strukturni udio (Donut Chart):** Prstenasti dijagram koji prikazuje proporcije prijava podijeljenih u četiri makro-vremenske cjeline dana (jutro, popodne, večer, noć) za odabranu godinu.
* **Narativna vizualizacija (Storytelling Engine):** Klikom na bilo koju aktivnu točku na karti ili grafu otvara se prilagođeni modalni prozor koji povlači i prikazuje izvorni tekstualni sinopsis i detaljno izvješće o incidentu.

## Korišteni podaci

* `nuforc_first_1000.csv`: Strukturirani podskup od 1000 kronološki mapiranih zapisa preuzetih iz baza podataka **NUFORC** (National UFO Reporting Center).
* `us-states.json`: GeoJSON topološka datoteka s koordinatama i granicama saveznih država SAD-a za iscrtavanje bazne karte.

## Tehnologije i arhitektura

* **Vizualizacija:** D3.js (Data-Driven Documents) v3
* **Stil i dizajn:** CSS3 s modernom, minimalističkom tamnom temom (Dark Mode) optimiziranom za taktičke preglede podataka.
* **Upravljanje podacima:** Klijentsko čišćenje podataka u *runtime* memoriji (dinamički parser tekstualnih trajanja u sekunde, standardizacija stringova, otklanjanje ekscesnih anomalija).

## 💻 Kako pokrenuti projekt lokalno?

Budući da D3.js povlači lokalne datoteke (`.csv` i `.json`) putem asinkronih HTTP zahtjeva (AJAX), preglednici iz sigurnosnih razloga (CORS politika) blokiraju izravno otvaranje `index.html` datoteke dvostrukim klikom s diska.

Za ispravno pokretanje potrebno je podići lokalni web poslužitelj:

1. Otvorite mapu projekta u **Visual Studio Code-u**.
2. Instalirajte ekstenziju **Live Server**.
3. Kliknite na gumb **"Go Live"** u donjem desnom kutu sučelja.

Projekt je izrađen u sklopu kolegija _Vizualizacija podataka_.
