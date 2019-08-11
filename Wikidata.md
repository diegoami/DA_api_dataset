# WIKIMEDIA

# QUERY IN CURL

```
curl --header "Accept: application/sparql-results+json"  -G 'https://query.wikidata.org/sparql' --data-urlencode query='
SELECT ?q ?qLabel ?cast_member ?cast_memberLabel WHERE {
  ?q wdt:P31 wd:Q11424.
  ?q wdt:P161 ?cast_member.
  SERVICE wikibase:label {
     bd:serviceParam wikibase:language "en" .
  }
}
LIMIT 100
'
```

## HUMANS

### QUERY

```
SELECT ?human WHERE {
  ?human wdt:P31 wd:Q5;
    wdt:P106 wd:Q713200.
}
```
### CATEGORIES

* performing artist (Q713200): 10158
* author (Q482980): 33353
* actor (Q33999):  211367
* film actor(Q10800557): 60749
* singer(Q177220) : 88543


## SUBJECT

```
SELECT ?q WHERE { ?q wdt:P31 wd:Q11424. }
```

### CATEGORIES

* movies(Q11424): 234349
* books(Q571): 68279
* song(Q7366): 55533
* video game(Q7889) : 38003
* website(Q35127): 9271

### SUBJECT WITH OPTION

Movie
```
SELECT ?q ?cast_member ?cast_memberLabel WHERE {
  ?q wdt:P31 wd:Q11424.
  OPTIONAL { ?q wdt:P161 ?cast_member. }
}
945970
SELECT ?q ?qLabel ?cast_member ?cast_memberLabel WHERE {
  ?q wdt:P31 wd:Q11424.
  ?q wdt:P161 ?cast_member.
  SERVICE wikibase:label {
     bd:serviceParam wikibase:language "en" .
  }
}
LIMIT 100
```

Video game
```
SELECT ?q ?cast_member ?cast_memberLabel WHERE {
  ?q wdt:P31 wd:Q7889.
  OPTIONAL { ?q wdt:P725 ?cast_member. }
}
```

Tv Show
```
SELECT ?q ?cast_member ?cast_memberLabel WHERE {
  ?q wdt:P31 wd:Q5398426.
  OPTIONAL { ?q wdt:P161 ?cast_member. }
}
```

Animated Film
```
SELECT ?q ?cast_member ?cast_memberLabel WHERE {
  ?q wdt:P31 wd:Q202866.
  OPTIONAL { ?q wdt:P725 ?cast_member. }
}
```

### ROLES IN MOVIE

```
SELECT ?film ?role ?person  WHERE {
  ?film wdt:P31 wd:Q11424;
    wdt:P57|wdt:P161|wdt:P162|wdt:P1431|wdt:P58|wdt:P344|wdt:P1040|wdt:P86|wdt:P2515|wdt:p2554|wdt:P170|wdt:P725 ?person.
  }
  ?person ?role ?film.
  
}
```
>1m 

### ROLES IN VIDEO SHOW

```
SELECT ?tv_series ?role ?person  WHERE {
  ?tv_series wdt:P31 wd:Q5398426;
    wdt:P57|wdt:P161|wdt:P162|wdt:P1431|wdt:P58|wdt:P344|wdt:P1040|wdt:P86|wdt:P2515|wdt:p2554|wdt:P170|wdt:P725 ?person.
  ?tv_series ?role ?person.
}
```

### ROLES IN ANIMATED MOVIES 

```

SELECT ?animated_movie ?role ?person  WHERE {
  ?animated_movie wdt:P31 wd:Q202866;
    wdt:P57|wdt:P161|wdt:P162|wdt:P1431|wdt:P58|wdt:P344|wdt:P1040|wdt:P86|wdt:P2515|wdt:p2554|wdt:P170|wdt:P725 ?person.
  ?animated_movie ?role ?person.
}

```
10319


### ROLES IN SONGS

```
SELECT ?person ?role ?song WHERE {
 
  ?person wdt:P175|wdt:P86|wdt:p676 ?song;
          wdt:P31/wdt:P279* wd:Q2188189.
  ?person ?role ?song.
  
}
# 413194
```


### ROLES IN GAMES

```
SELECT ?game ?role ?person  WHERE {
  ?game wdt:P31 wd:Q7889;
    wdt:P50|wdt:P58|wdt:P162|wdt:P86|wdt:P725  ?person.
  ?game ?role ?person.
}
```
6640

### VOICE CHARACTERS IN GAMES

```
SELECT ?game ?character  ?person  WHERE {
  ?game wdt:P31 wd:Q7889.
  ?game wdt:P674 ?character. 
  ?character wdt:P725 ?person.
}

```

### BOOKS

```

SELECT ?book ?role ?person  WHERE {
  
  
  ?book wdt:P31 wd:Q571.
  ?book wdt:P50|wdt:P2085381 ?person.
  ?book ?role ?person
}

```


