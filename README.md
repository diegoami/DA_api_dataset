# DA_api_dataset
Collection of APIs and Datasets for selected topics

**Good**, _Reasonable_, ~~Useless~~ 


## PODCASTS

### DATASETS


* **https://data.world/brandon-telle/podcasts-dataset**
* _https://www.kaggle.com/listennotes/all-podcast-episodes-published-in-december-2017_

### APIs

* **https://www.listennotes.com/api/**

## MOVIES



### DATASETS

* _https://datahub.io/collections/movies-and-tv_
* _https://www.kaggle.com/rounakbanik/the-movies-dataset_
* _https://www.kaggle.com/netflix-inc/netflix-prize-data_

### API


### WIKIDATA

#### MOVIES

```
SELECT ?q WHERE { ?q wdt:P31 wd:Q11424. }
```

#### ACTORS

```
SELECT ?human  WHERE {
  ?human wdt:P31 wd:Q5;
    wdt:P106 wd:Q33999.
}
```

```
SELECT ?human ?given_name WHERE {
  ?human wdt:P31 wd:Q5;
    wdt:P106 wd:Q33999.
  OPTIONAL{?human wdt:P735 ?given_name .}    
}
```

## COMPUTER GAMES

### API

* **https://www.igdb.com/api**
* _https://www.giantbomb.com/api/_

### WIKIDATA

```
SELECT ?q WHERE { ?q wdt:P31 wd:Q7889. }
```

### STEAM

* **https://www.reddit.com/r/Steam/comments/6nw75r/is_there_anyway_to_get_all_the_appid_of_steam/ **
* **https://steamcommunity.com/dev**


## BOOKS

### API

* **https://developers.google.com/books/**
**
### WIKIDATA

```
SELECT ?q WHERE { ?q wdt:P31 wd:Q571. }
```

## SONGS

### WIKIMEDIA


```
SELECT ?q WHERE { ?q wdt:P31 wd:Q7366. }
55533 songs
```


## LANGUAGES

## GEOGRAPHY


## CHESS
