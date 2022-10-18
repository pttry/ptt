
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
      default_encoding = "UTF-8",
      insert_native_pipe_operator = TRUE
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
   Omien tietojen antaminen git:lle:
4. `usethis::use_git_config(user.name = "YourName", user.email = "your@mail.com")`
   git tarvii access tokenin, jotta se voi kommunikoida githubin kanssa (Enemmän tietoa: https://happygitwithr.com/connect-intro.html)
5. `usethis::create_github_token()`
6. Tässä välissä avautuu selain ja kysytään githubin salasanaa ja pyydetään tietoja tokenin luomiseen. Note kohtaan esim mille tietokoneelle luot tokenin. Expiration on erääntymispäivä. Suositus on 30, mutta voi sen antaa pidemmäksikin, ikuista ei kuitenkaan kannata luoda. Token pitää luoda aina uudelleen erääntymispäivän jälkeen. Scope kannataa jättää oletusasetuksiin. Generate token avaan sivu, jolta tokenin voi kopioida. Jätä sivu auki.
8. `gitcreds::gitcreds_set()` kysyy uutta salasanaa tai tokenia. Kopioi siihen uusi luotu token sivulta.
9. Käynnistä R uudelleen. Voi testata: `usethis::git_sitrep()`

Projektin tuominen githubista:
1. File -> New project -> Version control -> Git
2. Lisää url githubista.
