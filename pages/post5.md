Impressions
---

Here I thought I'd just do something simple and make some word-clouds for each genre. There's not much too this, I just catenated all the overviews in any given genre and calculated the frequencies of every word. The specific frequency is then that value divided by the frequency of that word in the total data set. So if the word 'Sherlock' occurs 5 times in the mystery genre out of 100 total words, and 5 times in the total set of overviews, out of 1000 words, its specific frequency in mystery is 10.

Name tokens like this (i.e. 'Sherlock,' 'Scooby,' 'Poirot,' 'Kolchak' in the mystery genre) will often have the highest genre-specific-frequencies, so we only accept tokens which occur more than 100 times in the total data set. Then our word clouds look about right with words like 'investigate,' 'murder,' and 'detective.'

Here is a little thumbnail gallery.


**Action** | **Adventure** | **Animation**
[![action](../assets/post5/thumbnails/Action.png)](https://poptcorn.github.io/assets/post5/fullsize/Action.jpg) | [![adventure](../assets/post5/thumbnails/Adventure.png)](https://poptcorn.github.io/assets/post5/fullsize/Adventure.jpg) | [![animation](../assets/post5/thumbnails/Animation.png)](https://poptcorn.github.io/assets/post5/fullsize/Animation.jpg)
**Comedy** | **Crime** | **Documentary**
[![comedy](../assets/post5/thumbnails/Comedy.png)](../assets/post5/fullsize/Comedy.jpg) | [![crime](../assets/post5/thumbnails/Crime.png)](../assets/post5/fullsize/Crime.jpg) | [![documentary](../assets/post5/thumbnails/Documentary.png)](../assets/post5/fullsize/Documentary.jpg)
**Drama** | **Family** | **Fantasy**
[![drama](../assets/post5/thumbnails/Drama.png)](../assets/post5/fullsize/Drama.jpg) | [![family](../assets/post5/thumbnails/Family.png)](../assets/post5/fullsize/Family.jpg) | [![fantasy](../assets/post5/thumbnails/Fantasy.png)](../assets/post5/fullsize/Fantasy.jpg)
**Foreign** | **History** | **Horror**
[![foreign](../assets/post5/thumbnails/Foreign.png)](../assets/post5/fullsize/Foreign.jpg) | [![history](../assets/post5/thumbnails/History.png)](../assets/post5/fullsize/History.jpg) | [![horror](../assets/post5/thumbnails/Horror.png)](../assets/post5/fullsize/Horror.jpg)
**Music** | **Mystery** | **Romance**
[![music](../assets/post5/thumbnails/Music.png)](../assets/post5/fullsize/Music.jpg) | [![mystery](../assets/post5/thumbnails/Mystery.png)](../assets/post5/fullsize/Mystery.jpg) | [![romance](../assets/post5/thumbnails/Romance.png)](../assets/post5/fullsize/Romance.jpg)
**Science Fiction** | **Thriller** | **TV Movie**
[![science fiction](../assets/post5/thumbnails/Science Fiction.png)](../assets/post5/fullsize/Science Fiction.jpg) | [![thriller](../assets/post5/thumbnails/Thriller.png)](../assets/post5/fullsize/Thriller.jpg) | [![tv movie](../assets/post5/thumbnails/TV Movie.png)](../assets/post5/fullsize/TV Movie.jpg)
**War** | **Western**
[![war](../assets/post5/thumbnails/War.png)](../assets/post5/fullsize/War.jpg) | [![western](../assets/post5/thumbnails/Western.png)](../assets/post5/fullsize/Western.jpg)




---
---
I’d like to thank the themoviedb.org folks, who gave me access to their API which was relatively painless to use. I am not affiliated with them in any way and my opinions are my own. I’d also like to thank the developers and maintainers of: Python, word_cloud, and matplotlib.

[themoviedb](https://www.themoviedb.org) | [python](https://www.python.org) | [word_cloud](https://www.github.com/amueller/word_cloud) | [matplotlib](https://www.matplotlib.org)
![the movie db](../assets/credit/tmdb.png) | ![python](../assets/credit/python.png) | ![word_cloud](../assets/credit/word_cloud.png) | ![matplotlib](../assets/credit/mpl.png)


<!--

---
---



---
# Mystery
![Mystery](../assets/post5/fullsize/Mystery.png)


---
# Documentary
![Documentary](../assets/post5/fullsize/Documentary.png)

---
# Foreign
![Foreign](../assets/post5/fullsize/Foreign.png)

---
# Drama
![Drama](../assets/post5/fullsize/Drama.png)

---
# Animation
![Animation](../assets/post5/fullsize/Animation.png)

---
# Action
![Action](../assets/post5/fullsize/Action.png)

---
# Music
![Music](../assets/post5/fullsize/Music.png)

---
# Fantasy
![Fantasy](../assets/post5/fullsize/Fantasy.png)

---
# Romance
![Romance](../assets/post5/fullsize/Romance.png)

---
# Crime
![Crime](../assets/post5/fullsize/Crime.png)

---
# Adventure
![Adventure](../assets/post5/fullsize/Adventure.png)

---
# History
![History](../assets/post5/fullsize/History.png)

---
# TV Movie
![TV Movie](../assets/post5/fullsize/TV Movie.png)

---
# Comedy
![Comedy](../assets/post5/fullsize/Comedy.png)

---
# Science Fiction
![Science Fiction](../assets/post5/fullsize/Science Fiction.png)

---
# Western
![Western](../assets/post5/fullsize/Western.png)

---
# Family
![Family](../assets/post5/fullsize/Family.png)

---
# Horror
![Horror](../assets/post5/fullsize/Horror.png)

---
# War
![War](../assets/post5/fullsize/War.png)

---
# Thriller
![Thriller](../assets/post5/fullsize/Thriller.png)


-->
