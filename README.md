# Natūralios kalbos apdorojimo projektinė užduotis

Sukurkite programą, kuri rastų tekste dažniausiai pasitaikančius žodžius, išskyrus nereikšmingus žodžius. (angl. stop words)

# Užduoties realizavimas

## Tekstiniai failai

Šiai užduočiai atlikti naudojami 2 tekstiniai failai - “Stopwords.txt” ir “Text.txt”. “Stopwords” failo turinys yra toks: the, of, and, in, a, by, its, was, to, at, as, it, has, but, not. Tai nereikšmingi žodžiai, kurie nėra skaičiuojami kaip dažniausiai pasikartojantys žodžiai tekste. “Text” failo turinys - tai tekstas, kuris yra nagrinėjamas. Simboliška, kadangi pasirinktas tekstas apie Vilniaus universitetą anglų kalba.

## Bibliotekos

Užduočiai atlikti naudojamos 3 bibliotekos (žr. pav. nr. 1):
import collections - importuojamos talpyklos, kuriose galima saugoti duomenis, jų kolekcijas (pavyzdžiui list, dict, set, tuple).
import pandas - leidžia pateikti duomenis tokiu būdu, kuris yra tinkamas duomenų analizei
import mathplotlib.pyplot - leidžia naudotis MATLAB programos privalumais: leidžia sukurti figūras, linijas, etiketes ir panašiai.

## Programos kodas

* Pirma, nuskaitomas failas, su nurodyta koduote. UTF-8 koduotė - viena kintamo ilgio simbolių koduočių, kuria galima užrašyti bet kokį Unikodo simbolį.

* Nustatomi žodžiai, kurie nebus skaičiuojami kaip dažniausiai pasikartojantys. Tai vadinamieji “nereikšmingi žodžiai”. Vartotojas gali pats papildyti nereikšmingų žodžių sąrašą. Tai rodo programos lankstumą, tačiau atneša ir šiokių tokių trūkumų (pateikiama skyriuje “Testavimo išvados”).

* Sukuriamas naudojamo teksto žodynas: jei žodis tame tekste yra naujas, jis įrašomas į žodyną, jeigu jau egzistuoja, padidinamas jo kiekis.

* Norint eliminuoti dublikatus (pavyzdžiui Vilnius, Vilnius ir Vilnius:) pašalinami simboliai, sumažinamos didžiosios raidės. Sukuriamas ankstesniame žingsnyje minėtas teksto žodynas.

* Vartotojui leidžiama pasirinkti kiek dažniausiai pasikartojančių žodžių spausdinti. Atspausdinami rezultatai.

* Pagal visas gerąsias programavimo praktikas uždarytą failą reikia uždaryti.

## Programinė įranga

Programos kūrimui, testavimui, rezultatų atvaizdavimui - projekto kūrimui pasirinkta naudoti Jupyter NoteBook. Tai patogus, greitas darbo įrankis, leidžiantis ne tik matyti tekstinius, tačiau ir vizualizuotus rezultatus.

## Testavimo išvados

Programa gana nesudėtinga, tad gerai tvarkosi su nedidelės apimties tekstais, kurie naudoja pagrindinius skyrybos ženklus ir yra parašyti anglų kalba. Didelis programos trūkumas yra tas, kad kiekvieną skyrybos ženklą programoje reikia apibrėžti - didėja žmogiškos klaidos galimybė. Jeigu ši programa būtų naudojama didelės apimties tekstų analizei ir dažniausiai pasikartojančių žodžių paieškai, tikrai būtų ir klaidų. Dėl programos lankstumo galimybės sudaryti savo nereikšmingų žodžių sąrašą kyla ir pliusų ir minusų: vartotojas gali lanksčiai rinktis nereikšmingų žodžių rinkinį, jį sudaryti pagal save, tačiau dirbant su didelės apimties tekstais gali būti sunku apibrėžti visus norimus žodžius ir gali užtrukti daug laiko.

## Rezultatų vizualizavimas

Programoje realizuota galimybė pasirinkti išvesties kiekį - kiek dažniausiai pasikartojančių žodžių atspausdinti. Pagal tai sudaroma diagrama, turinti 5 skirtingas spalvas. Jeigu atvaizduojami daugiau negu 5 stulpeliai, spalvos paeiliui kartojamos.
