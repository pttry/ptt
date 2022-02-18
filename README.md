
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
5. Käynnistä Rstudio uudelleen.

## robonomistin käyttö PTT:llä

Ohjeita: https://pttry.github.io/pttrobo/

## git ja githubin käyttö

Asennus ja käyttöön otto:
1. Asenna git koneelle: https://git-scm.com/download/win
2. Rstudiossa: Tools -> Global options..-> Git/SVN ja raksi ruutuun enable. Polku git:iin pitäisi olla ruudussa alla.
3. `install.packages(c("usethis", "gitcreds"))`
4. `usethis::use_git_config(user.name = "YourName", user.email = "your@mail.com")`
5. `usethis::create_github_token()`
6. Tässä välissä kysyy salasanaa selaimessa
7. `gitcreds::gitcreds_set()`
8. `credentials::set_github_pat()`

Projektin tuominen githubista:
1. File -> New project -> Version control -> Git
2. Lisää url githubista.
