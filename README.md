# TDAP harjoituspohja
Repo sisältää Tilastollisen data analyysin perusteet kurssin
harjoitus- ja viikkotehtäväraporttien pohjan rmarkdown muodossa.

## Tarvittavat paketit
RMarkdownin käyttämiseksi, R:llä tulee asentaa seuraavat paketit

```{R}
install.packages('rmarkdown')
install.packages('tinytex')
tinytex::install_tinytex()
```

## Pohjan käyttäminen
Pohjaa voidaan käyttää helposti kopioimalla `pohja.Rmd` ja kirjoittamalla
RMarkdownilla se, jonka jälkeen RMarkdown tiedosto käännetään pdf:ksi.

Käyttäjän tulee käydä ja vaihtaa `template/title.sty` tiedostosta nimi
Matti Meikäläinen ja opiskelijanumero oikeiksi.

## Harjoitustiedoston kääntäminen
Harjoitustiedosto voidaan kääntää pdf:ksi kahdella tapaa, joko
R istunnossa, jolloin pitää huomioida istunnossa jo olevat muuttujat.

```{R}
rmarkdown::render('harjoitus1.Rmd')
```

Tai voidaan hyödyntää repossa olevaa bash skriptiä `bin/create`

```{bash}
bin/create harjoitus1
```

## Keihtysehdotukset
Pohjaa saa vapaasti kehittää eteenpäin ja pull requestit otetaan mielellään
vastaan.
