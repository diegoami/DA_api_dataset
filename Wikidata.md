# WIKIMEDIA

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
