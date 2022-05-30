# Srpski LaTeX šablon

Minimalan kôd koji je želite da napišete pre pisanja bilo kog LaTeX rada na srpskom. Ovaj šablon koristi [XeTeX](https://en.wikipedia.org/wiki/XeTeX) kompajler da bi omogućio ravnopravno korišćenje latinice i ćirilice (ali i svih drugih evropskih i svetskih pisama), bez potrebe za korišćenjem komplikovanih TeX naredbi poput `\vc`, `\sh`, `\tj`, itd... Kratko rečeno, šablon funkcioniše po principu *Piši kao što govoriš, kompajliraj kako je napisano.*

## Napomene

### Kompilacija 

Fajl `main.tex` je potrebno kompajlirati sa XeTeX kompajlerom. Ovaj kompjaler dolazi uz svaku TeX distribuciju, te i vaše TeX okruženje može kompajlirati priloženi kôd. Pogledajte dokumentaciju vašeg TeX okruženja za više detalja o tome kako podesiti XeTeX kompajler.

Ako kompajlirate u konzoli, dovoljno je da pokrenete

```bash
xelatex main.tex
```

### Fontovi

Šablon koristi *unicode* verziju "standardnog" TeX fonta [*Computer Modern*](https://en.wikipedia.org/wiki/Computer_Modern). Font *Computer Modern Unicode* sadrži sva srpska slova (ali i slova mnogih drugih svetskih jezika). Ovaj font bi trebalo da bude instaliran sa vašom TeX distribucijom.

Ako želite da promenite font navedite ime drugog fonta u okviru komande `\setmainfont{}`. Neophodno je da odaberete font koji sadrži sve glifove koje koristite!

### Lokalizacija

Lokalizovani nazivi koje TeX automatski generiše (naslov sadržaja, potpisi slika i tabela, datumi, početak `proof` okruženja, itd...) će biti ispisani ćirilicom. Ako želite latinične nazive, liniju `\setmainlanguage{serbian}` promenite u `\setmainlanguage[Script=Latin]{serbian}`.

Lokalizaciju okrženja za teoreme, leme, primere, itd, ručno izvršite pomoću komande `\newtheorem`.

### Slike

Komandom `\graphicspath` je osigurano da se sve slike učitavaju iz `img/` direktorijuma. Stoga, za učitavanje slike `img/slika.png` je potrebno napisati `\includegraphics{slika.png}` a ne `\includegraphics{img/slika.png}`. Na ovaj način je bolje organizovan projekat.

Ako ne želite opisanu funkcionalnost, uklonite liniju `\graphicspath{{img/}}`.

### Razlika između LaTeX i XeLaTeX koda

Komande koje ste do sada koristili u LaTeX dokumentima za formatiranje teksta i matematičkih izraza možete koristiti i dalje bez problema. Korišćenje nekih starijih paketa može stvoriti probleme ako se ti paketi oslanjaju na TeX kodiranja.

### Bibliografija

Za obradu bibliografije [koristite](https://www.overleaf.com/learn/latex/Articles/Getting_started_with_BibLaTeX) `biblatex` paket.

## Učitani paketi

 + [amsmath](https://ctan.org/pkg/amsmath), [amsthm](https://ctan.org/pkg/amsthm), [amssymb](https://ctan.org/pkg/amsfonts) - poboljšana matematička tipografija
 + [fontspec](https://ctan.org/pkg/fontspec) - učitavanje fontova
 + [graphicx](https://ctan.org/pkg/graphicx) - učitavanje i elementarena manipulacija grafičkih datoteka (`.png`, `.jpg`, `.eps`, `.pdf`...)
 + [hyperref](https://ctan.org/pkg/hyperref) - podrška za PDF linkove i PDF sadržaj
 + [polyglossia](https://ctan.org/pkg/polyglossia) - lokalizacija i prelom
 + [xcolor](https://ctan.org/pkg/xcolor) - boje

