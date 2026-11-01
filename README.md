# algoritmitAI
algoritmit-ja-tekoaly-harjoitustyo

Jälki-ilmoittautuminen kurssille 28.10. , kurssityön suunnittelu aloitettu 1.11.

# Määrittelydokumentti

- **Opinto-ohjelma:** Tietojenkäsittelytieteen kandidaatti (TKT)
- **Dokumentaation kieli:** Suomi
- **Ohjelmointikieli:** Python
- **Muut hallittavat kielet vertaisarviointiin:** Pystyn vertaisarvioimaan Pythonilla toteutettuja, suomeksi tai englanniksi dokumentoituja projekteja.

## Harjoitustyön ydin
Harjoitustyön ydin on tekstihakumoottorin keskeisten tietorakenteiden (Trie-puu ja käänteisindeksi) sekä kahden relevanssialgoritmin (Okapi BM25 ja TF-IDF) toteuttaminen ja vertailu. Työssä keskitytään hakurakenteiden ja pisteytyslogiikan ohjelmointiin sekä testaamiseen, ei käyttöliittymään tai tiedostojen käsittelyyn.   

## Ratkaistava ongelma
Tekoälyhakukoneet ja RAG-järjestelmät (*Retrieval-Augmented Generation*) etsivät verkkosivuilta kyselyyn parhaiten sopivat tekstikappaleet kielimallin lähdeaineistoksi. Ohjelma auttaa arvioimaan verkkosivusisältöjen löydettävyyttä (GEO, *Generative Engine Optimization*) indeksoimalla tekstikappaleet ja vertailemalla, miten BM25 ja TF-IDF pisteyttävät niitä annetuilla hakukyselyillä.

## Toteutettavat algoritmit ja tietorakenteet
- **Trie (Etuliitepuu):** Puutietorakenne sanaston tallentamiseen ja hakusanojen nopeaan etsimiseen.
- **Käänteisindeksi (Inverted Index):** Tietorakenne, joka yhdistää jokaisen sanan niihin tekstikappaleisiin, joissa sana esiintyy, sekä tallentaa esiintymismäärät.
- **Okapi BM25 ja TF-IDF:** Kaksi tiedonhakualgoritmia, jotka laskevat tekstikappaleille relevanssipisteet hakusanojen yleisyyden, harvinaisuuden ja kappaleen pituuden perusteella.

## Ohjelman syötteet ja niiden käyttö
- **Tekstiaineisto:** Ohjelma lukee tekstitiedostoja (esim. verkkosivujen tekstejä), jakaa ne kappaleisiin ja indeksoi sanat Trie-puuhun sekä käänteisindeksiin.
- **Hakukysely:** Käyttäjä syöttää hakulausekkeen komentoriviltä, minkä jälkeen ohjelma laskee osumille BM25- ja TF-IDF-pisteet ja tulostaa parhaat tekstikappaleet paremmuusjärjestyksessä.

## Tavoitteena olevat aika- ja tilavaativuudet
- **Trie-haku ja -lisäys:** Aikavaativuus on $O(m)$, missä $m$ on sanan pituus.
- **Indeksointi:** Aikavaativuus on $O(T)$, missä $T$ on aineiston sanojen kokonaismäärä, ja tilavaativuus on $O(V + P)$, missä $V$ on sanaston koko ja $P$ esiintymälistojen pituus.
- **Haku ja pisteytys:** Aikavaativuus on $O(N \log N)$, missä $N$ on hakusanoja sisältävien tekstikappaleiden määrä.
