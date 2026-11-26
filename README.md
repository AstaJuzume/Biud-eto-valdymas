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

## Atskiro ataskaitos prototipo susiejimas

Ataskaita kuriama ir talpinama atskirai. Kai bus paruošta jos nuoroda, faile `config.js` užpildykite:

```javascript
window.VERSINA_CONFIG = {
  reportUrl: "https://jusu-ataskaitos-prototipas.example"
};
```

Aplikacijos šoniniame meniu automatiškai atsiras nuoroda **Ataskaita**, atidaranti prototipą naujame skirtuke. Kol `reportUrl` tuščias, nuoroda nerodoma. Abu prototipai turi savo atskirus duomenis ir prieigos nustatymus; nuoroda duomenų nesinchronizuoja.

## Failai

- `index.html` – aplikacijos pradžia.
- `app.js` – demonstraciniai duomenys ir aplikacijos funkcijos.
- `style.css` – adaptyvi „Power Apps“ stiliaus sąsaja.
- `config.js` – atskiros ataskaitos prototipo nuoroda.
