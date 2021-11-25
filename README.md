
# ptt

<!-- badges: start -->
<!-- badges: end -->

ptt paketti on metapaketti R-työskentelyyn PTT:ssä.

Paketti ainoastaan lataa tarvittavat erilliset paketit ja on alusta ohjeille.

Ladattavat paketit ovat:

- pttrobo

## Asennus

You can install the development version of ptt from [GitHub](https://github.com/) with:

``` r
# install.packages("devtools")
devtools::install_github("pttry/ptt")
```

## Ohjeet

### Asennus ja asetukset

1. Lataa ja asenna R ja Rstudio: https://www.rstudio.com/products/rstudio/download/#download
2. Hae .Rprofile tiedosto teamsista () ja tallenna oman koneen Tiedostot kansioon.
   Se sisältää sisäänpääsykoodin robonomistin palvelimeen, joten sitä ei pidä jakaa
   ulkopuolisille.
3. Asenna tämä paketti: `install.packages("devtools"); devtools::install_github("pttry/ptt", dependencies = TRUE)`
4. Muuta Rstudio asetukset ajamalla seuraava koodi R:ssä:


```r

   rstudio.prefs::use_rstudio_prefs(
      save_workspace = "never",
      load_workspace = FALSE,
      rainbow_parentheses = TRUE,
      default_encoding = "UTF-8"
   )
``` 

