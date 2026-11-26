# VERSINA · Objektų biudžetų kontrolė

Interaktyvus „Power Apps“ stiliaus prototipas statybos objektų biudžetų planavimui ir faktinių sąnaudų peržiūrai.

## Funkcijos

- Objektų registras ir objekto kortelė.
- Bendro biudžeto bei mėnesio išlaidų ir aktavimo planavimas.
- Mėnesio plano pogrupiai ir komentarai.
- Plano ir fakto palyginimas, biudžeto likučiai ir viršijimai.
- Biudžeto perskirstymas tarp grupių išlaikant bendrą sumą ir pakeitimų istoriją.
- Demonstracinių HANSA dokumentų, medžiagų likučių ir avansų peržiūra.
- Mėnesio ataskaita, spausdinimas, CSV importas ir eksportas.
- Projekto ir įmonės vadovų demonstraciniai vaidmenys.

Tai HTML, CSS ir JavaScript demonstracija, ne eksportuota „Power Apps“ aplikacija. Duomenys pavyzdiniai. Pakeitimai išsaugomi tik konkrečios naršyklės vietinėje saugykloje. Prisijungimas, prieigos teisės ir tikra HANSA integracija neįgyvendinti.

## Paleidimas

Nereikia diegti priklausomybių ar vykdyti build. Atidarykite `index.html` arba paleiskite statinį HTTP serverį:

```bash
python3 -m http.server 8000
```

## GitHub Pages

Repozitorijos Settings → Pages pasirinkite Deploy from a branch, šaką `main` ir katalogą `/ (root)`. Visi resursų keliai santykiniai, todėl aplikacija palaiko repozitorijos `/Versina/` kelią.

## Ataskaitos prototipas

Ataskaita įkelta į `ataskaita.html` ir laikoma kartu su aplikacija. Aplikacijos šoniniame meniu spustelėjus **Ataskaita**, ji atidaroma naujame skirtuke. Ataskaitos viršuje yra nuoroda **Grįžti į aplikaciją**.

`config.js` nurodytas santykinis kelias `./ataskaita.html`, todėl susiejimas veikia ir repozitorijos `/Versina/` kelyje. Norint ateityje ataskaitą talpinti kitur, šį kelią galima pakeisti visa HTTPS nuoroda. Kol `reportUrl` tuščias, meniu nuoroda nerodoma.

Abu prototipai turi atskirus demonstracinius duomenis; nuoroda duomenų nesinchronizuoja. Ataskaita nėra tikra Power BI integracija.

## Failai

- `index.html` – aplikacijos pradžia.
- `app.js` – demonstraciniai duomenys ir aplikacijos funkcijos.
- `style.css` – adaptyvi „Power Apps“ stiliaus sąsaja.
- `config.js` – ataskaitos prototipo nuoroda.
- `ataskaita.html` – interaktyvus ataskaitos prototipas su filtrais ir detalia peržiūra.
