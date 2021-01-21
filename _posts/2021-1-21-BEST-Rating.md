---
layout: post
title:  "BEST Rating System "
date:   2021-01-21 17:31:35 -0500
categories: TV Shows
---
I enjoy watching TV and movies in my free time. I have watched so many great TV shows and films over the years, and I wanted to create a way for me to rank them. I decided to create the **BEST** Rating system to categorize my favorite TV shows and movies! 10 points for each category (BEST), and the average will be calculated to determine the show's or movie's overall rank.
## <ins>**B**</ins>eginning
It normally takes me the 1st scene to know if a movie or TV show is worth watching. It needs to grasps the viewer's attention within the first 10 seconds. In this category, I will take into account the theme song, pilot episode, and the trailer.
## <ins>**E**</ins>nsemble
The cast is one of the most important parts of making a project happen. Without the actors there would be no movie or TV show. I will evaluate the cast chemistry as well as the individual characters and their arcs.
## <ins>**S**</ins>toryline
The plot of any movie or TV show has to be interesting enough to initally watch it. The story should be compelling from the synopsis/ tagline. I will rate the overall story as a whole and highlight my favorite plot twists and unexpected endings. 
## <ins>**T**</ins>alk
The dialogue and the way the actors present the script are extremely important. The way the actors speak must be believable in order to convey any type of emotion. I will observe how the characters speak to one another, the inner dialogue, as well as the nonverbal communication.
## Method 1
Python function to calculate the rating from an input for each category. 
``` python
def best_rating_m1(b,e,s,t):
  score = ((b + e + s + t)/4.0)
  return score
```
## Method 2
Simple way of doing the above calculations by using a lambda function that can take any number of arguments (b, e, s, t) and returns the average of the values. It is written with one line of code as opposed to the 3 lines in Method 1.

``` python
best_rating_m2 = lambda b,e,s,t: ((b + e + s + t)/4.0)
```
Replace # with a number (0-10) points you have for each category (beginning , ensemble , storyline , talk).
``` python
tvshow1 = best_rating_m2(#, #, #, #)
tvshow2 = best_rating_m2(#, #, #, #)
...
tvshown = best_rating_m2(#, #, #, #)
```

A dictionary is then created to keep track of the overall rating for each TV show or movie. 
``` python
rating_list = {'TV show 1' : tvshow1, 'TV show 2' : tvshow2, ... , 'TV show n' : tvshown}
print(rating_list)
```

A bar chart is created to visualize the ratings and rank the Top 5 favorite TV shows or movies from Best to Worst.
``` python
# Plot a bar chart to visualize the rating
import matplotlib.pyplot as plt
# Sort the list to show highest ranked shows first
lists = sorted(rating_list.items(), key=lambda x: x[1], reverse=True)
x, y = zip(*lists)
plt.bar(x, y)
# Limits for the Y axis
plt.ylim(0,10)
# Add title and axis names
plt.title('Graph Title')
plt.xlabel("X axis label")
plt.ylabel("Y axis label")
plt.show()
```
Based on the values you give for each show or movie, you should see a bar chart display with the highest ranked tv show or movie showing 1st.

In the next blog post, I will show how I rank my favorite Comedy-Crime/ Mystery shows fom Best to Worst using this rating system. 
