
# ptt

<!-- badges: start -->
<!-- badges: end -->

ptt paketti on metapaketti R-työskentelyyn PTT:ssä.

Paketti ainoastaan lataa tarvittavat erilliset paketit ja on alusta ohjeille.

Ladattavat paketit ovat:

- tidyverse,
- ggptt
- pttrobo
- pttdatahaku

## Asennus

You can install the development version of ptt from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("pttry/ptt")
```

## Ohjeet R:n ja ptt-pakettien käyttöönottoon

### Asennus ja asetukset

1. Lataa ja asenna R ja Rstudio: https://www.rstudio.com/products/rstudio/download/#download
2. Hae .Rprofile-tiedosto teamsista (Pellervon taloustutkimus/Koulutus/R/R-apu) ja tallenna se oman koneen Tiedostot kansioon. HUOM! tallennus yrittää poistaa pisteen tiedoston nimen edestä. Se täytyy lisätä.
   Se sisältää sisäänpääsykoodin robonomistin palvelimeen, joten sitä ei pidä jakaa
   ulkopuolisille. Jos sinulla on jo oma .Rprofile tiedosto voit lisätä sinne mallitiedostosta robonomist.server ja robonomist.access.token tiedot.
3. Asenna tämä paketti: `install.packages("devtools"); devtools::install_github("pttry/ptt", dependencies = TRUE)`. Asennus valittaa Rtools-ohjelman puutteesta, mutta sitä ei tarvita välttämättä.
4. Muuta Rstudio asetukset ajamalla seuraava koodi R:ssä:


```r

   rstudio.prefs::use_rstudio_prefs(
      save_workspace = "never",
      load_workspace = FALSE,
      rainbow_parentheses = TRUE,
      default_encoding = "UTF-8"
   )
``` 

## robonomistin käyttö PTT:llä

Ohjeita: https://pttry.github.io/pttrobo/
