# Srpski TeX šablon

Minimalan kod koji je želite da napišete pre pisanja bilo kog rada na srpskom. Ovaj šablon koristi [XeTeX](https://en.wikipedia.org/wiki/XeTeX) sistem da bi omogućio ravnopravno korišćenje latinice i ćirilice (i svih drugih pisama), bez potrebe za korišćenjem komplikovanih TeX naredbi poput `\vc`, `\sh`, `\tj`, itd...

## Napomene

### Kompilacija 

Fajl `main.tex` je potrebno kompajlirati sa XeTeX kompajlerom. Ovaj kompjaler dolazi uz svaku TeX distribuciju, te je gotovo sigurno da vaše TeX okruženje može kompajlirati XeTeX kod. Pogledajte dokumentaciju vašeg TeX okruženja za više detalja.

Ako kompajlirate u konzoli, dovoljno je da pokrenete

```bash
xelatex main.tex
```

### Fontovi

Šablon koristi *unicode* verziju "standardnog" TeX fonta *Computer Modern* koji sadrži sva srpska slova (ali i mnogih drugih svetskih jezika). Ovaj font bi trebalo da bude instaliran zajedno sa vašom TeX distribucijom.

Ako želite da promenite font, ili Vam je *Computer Modern Unicode* nedostupan, navedite ime drugog fonta u okviru komande `\setmainfont{}`. Neophodno je da odaberete font koji sadrži sve glifove koje koristite! 

### Lokalizacija

Lokalizovani nazivi koje TeX automatski generiše (naslov sadržaja, potpisi slika i tabela, datumi, početak `proof` okruženja, itd...) će biti ispisani ćirilicom. Ako želite latinične nazive, liniju `\setmainlanguage{serbian}` promenite u `\setmainlanguage[Script=Latin]{serbian}`.

Lokalizaciju okrženja za teoreme, leme, primere, itd,... ručno izvršite uz pomoć komande `\newtheorem`.

### Slike

Komandom `\graphicspath`je osigurano da se sve slike učitavaju iz `img/` direktorijuma. Stoga, za učitavanje slike `slika.png` je potrebno napisati `\includegraphics{slika.png}` a ne `\includegraphics{img/slika.png}`.

### Razlika između i TeX i XeTeX koda

Komande koje ste do sada koristili u LaTeX dokumentima za formatiranje teksta i matematike možete koristiti i dalje bez problema. Korišćenje nekih starijih paketa može stvoriti probleme ako se ti paketi oslanjaju na klasična TeX kodiranja.

### Učitani paketi

 + [amsmath](https://ctan.org/pkg/amsmath), [amsthm](https://ctan.org/pkg/amsthm), [amssymb](https://ctan.org/pkg/amssymb)
 + [fontspec](https://ctan.org/pkg/fontspec)
 + [graphicx](https://ctan.org/pkg/graphicx)
 + [hyperref](https://ctan.org/pkg/hyperref)
 + [polyglossia](https://ctan.org/pkg/polyglossia)
 + [xcolor](https://ctan.org/pkg/xcolor)


