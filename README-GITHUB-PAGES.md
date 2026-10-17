# Salibandy-TV – GitHub Pages -testiversio

Tämä on erillinen staattinen versio alkuperäisestä ZIP-paketista. Se ei sisällä Vercelin API-reittejä eikä muuta alkuperäistä Vercel-projektia.

## Julkaisu GitHub Pagesissa
1. Tee GitHubiin erillinen testirepositorio (tai käytä erillistä haaraa).
2. Pura tämän ZIP-paketin sisältö repositorion juureen.
3. Avaa repositorion **Settings → Pages** ja julkaise `Deploy from a branch` -asetuksella `main` / `/(root)`.
4. Avaa julkaistu `index.html`. Grafiikkojen URL-osoitteet ovat saman sivuston alla.

## Tärkeät rajoitukset
- Live-data haetaan suoraan selaimesta TorneoPalin `salibandy-api.torneopal.net`-rajapinnasta. Tämä onnistuu vain, jos TorneoPal sallii pyynnöt selaimen CORS-käytännöillä. GitHub Pages ei voi ohittaa CORS-estettä. Jos grafiikka näyttää CORS-/verkkovirheen, täysin GitHub Pages -pohjainen reaaliaikainen versio ei toimi ilman erillistä välityspalvelua.
- Oletusottelu ja grafiikkojen näkyvyys tallentuvat selaimen `localStorage`-muistiin. Ne eivät synkronoidu eri laitteiden, selainten tai OBS-koneen ja ohjauspaneelin välillä. Avaa ohjauspaneeli ja grafiikat samassa selaimen profiilissa/originessa, jos haluat jakaa paikalliset asetukset.
- Ohjauspaneelin salasana ei suojaa paikallista tallennusta tässä versiossa. Älä käytä tätä versiota etäohjaukseen tai yhteiseen tuotantolähetykseen ennen testejä. Nykyinen Vercel-versio säilyy ennallaan.
- Ulkoasut ja grafiikkatiedostot säilytetään alkuperäisestä paketista; `salibandy-tehopelaajat.html`-sivun `offsetY=105`-oletusta ei muuteta.

## Testaus
Testaa ensin `salibandy-getscore-getmatch-nopeustesti.html` ja sitten `salibandy-tulostaulu.html?match_id=953141`. Jos selaimen konsoli tai sivu ilmoittaa CORS-virheen, se on TorneoPalin rajapinnan selainkäyttöä koskeva rajoitus eikä GitHub Pages -julkaisun virhe.
