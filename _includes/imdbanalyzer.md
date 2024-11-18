Import libraries and load the CSV file with ratings.

You can obtain the ratings file from your IMDb user account.


```python
import pandas as pd 
import numpy as np
import matplotlib.pyplot as plt
from datetime import date

ratings  =  pd.read_csv("ratings.csv")

print("Last updated:" + str(date.today()))
```

    Last updated:2024-11-18
    

Parsing data.

Essentially, I will count the occurrences of each instance.

I am interested only in my own ratings, IMDb ratings, release year, and genres.

Please note that one movie can belong to multiple genres.


```python
movie_idxs          = ratings.index[ratings['Title Type']=='Movie'].tolist()

my_movie_ratings    = ratings.iloc[movie_idxs,1]
counted_ratings     = np.unique(my_movie_ratings, return_counts=True)

imdb_ratings        = ratings.iloc[movie_idxs,7]

my_movie_years      = ratings.iloc[movie_idxs,9]
counted_years       = np.unique(my_movie_years, return_counts=True)

my_movie_runtimes   = ratings.iloc[movie_idxs,8]
counted_runtimes    = np.unique(my_movie_runtimes, return_counts=True)

my_movie_genres_aux = ratings.iloc[movie_idxs,10].str.split(", ") # the space after the comma is important
my_movie_genres     = [item for sublist in my_movie_genres_aux for item in sublist]
counted_genres      = np.unique(my_movie_genres, return_counts=True)
```

Plotting the distribution of my ratings.

The total number of movies I have given each score is indicated on top of each bar.


```python
plt.figure(figsize=(6, 6), frameon=True)
plt.bar(counted_ratings[0], counted_ratings[1], color ='#4682B4', width = 0.5, edgecolor='wheat', linewidth=2)
 
plt.xlabel("My Rating")
plt.ylabel("Number of movies")
plt.xticks(counted_ratings[0])

for i in range(len(counted_ratings[0])):
    plt.text(counted_ratings[0][i], counted_ratings[1][i] + 10,
             str(counted_ratings[1][i]))

plt.title("I have watched a total of %d movies" %(sum(counted_ratings[1][:]))) 

plt.show()
```


    
![png](../images/imdbanalyzer_files/imdbanalyzer_5_0.png)
    


Plotting information about the genres.

For better visualization, I will group less-watched genres into *Others* and limit the pie chart to eight wedges.

The popularity of each genre in the *Others* category is listed in the table below.


```python
genres_dataframe = pd.DataFrame(
    data = {
        'Genre': counted_genres[0].tolist(),
        'value' : counted_genres[1].tolist()},
    ).sort_values('value', ascending = False)

# The top 7 most watched genres
genres_dataframe_most_watched = genres_dataframe[:7].copy()

# The remaining genres are summed up altogether
genres_dataframe_others = pd.DataFrame(data = {
    'Genre' : ['Others'],
    'value' : [genres_dataframe['value'][7:].sum()]
})

# Combine dataframes
genres_dataframe_compact = pd.concat([genres_dataframe_most_watched, genres_dataframe_others])

# I like blue :)
color_shades = ['#728FCE','#4863A0','#2B547E','#36454F', '#29465B','#2B3856','#123456', '#151B54']	

fig, ax = plt.subplots(figsize=(6, 6))

patches, texts, pcts = ax.pie(
    genres_dataframe_compact['value'], labels=genres_dataframe_compact['Genre'].tolist(), autopct='%.1f%%',
    colors=color_shades,
    wedgeprops={'linewidth': 2.0, 'edgecolor': 'wheat'},
    textprops={'size': 'large', 'fontweight': 'bold'})

# Set the corresponding text label color to the wedge's face color.
for i, patch in enumerate(patches):
    texts[i].set_color(patch.get_facecolor())

plt.setp(pcts, color='white')
plt.setp(texts, fontweight='bold')

ax.set_title('Most watched genres', fontsize=18)

plt.tight_layout()
plt.show()

genres_dataframe_less_watched = genres_dataframe[7:].copy()
genres_dataframe_less_watched.rename(columns = {'value':'Movies watched'}, inplace = True)
genres_dataframe_less_watched.style.set_table_styles(
    [
        {
            'selector': 'th',
            'props': [('background-color', '#D3D3D3')]
        },
    ]
)



print(genres_dataframe_less_watched.to_string(index=False))


```


    
![png](../images/imdbanalyzer_files/imdbanalyzer_7_0.png)
    


          Genre  Movies watched
         Sci-Fi             401
        Romance             297
        Fantasy             284
         Horror             264
         Family             179
      Biography             131
      Animation             117
            War              85
        History              78
        Western              37
          Sport              34
    Documentary              31
          Music              30
        Musical              28
      Film-Noir              14
    

In the following, I will plot the average rate for each genre.


```python
plt.figure(figsize=(6, 6))
 
plt.xlabel("Genre")
plt.ylabel("Average rating")

my_avg_genre_rating   = np.zeros([len(counted_genres[0])]) # Empty array
imdb_avg_genre_rating = np.zeros([len(counted_genres[0])]) # Empty array

for i, genre in enumerate(counted_genres[0]):
    for k in range(len(ratings['Genres'])):
        if (genre in str(ratings['Genres'][k])) and str(ratings['Title Type'][k]) == 'Movie':
            if genre == 'Music' and 'Musical' in str(ratings['Genres'][k]):
                # I am sure there's a better way to perform these loops :)
                pass
            else:
                my_avg_genre_rating[i] += ratings['Your Rating'][k]
                imdb_avg_genre_rating[i] += ratings['IMDb Rating'][k]

    my_avg_genre_rating[i] = my_avg_genre_rating[i]/counted_genres[1][i]
    imdb_avg_genre_rating[i] = imdb_avg_genre_rating[i]/counted_genres[1][i]

x_axis = np.arange(len(counted_genres[0]))
plt.bar(x_axis + 0.2, my_avg_genre_rating, width=0.4, label = 'Mine', color="#002c5a",edgecolor="sienna")
plt.bar(x_axis - 0.2, imdb_avg_genre_rating, width=0.4, label = 'IMDb', color="#96caff",edgecolor="maroon")
plt.xticks(x_axis,counted_genres[0])
plt.xticks(rotation=90)
plt.legend()
plt.grid(color = 'green', linestyle = '--', linewidth = 0.5)
plt.grid(axis = 'x')
plt.ylim([0, 10])
plt.show()
```


    
![png](../images/imdbanalyzer_files/imdbanalyzer_9_0.png)
    


As somewhat expected for someone born in 1990, I have been watching more recent movies.

Additionally, only a few classics have stood the test of time.


```python
plt.figure(figsize=(6, 6))
plt.bar(counted_years[0], counted_years[1], color ='#4682B4', width = 0.5, edgecolor="maroon",linewidth = 0.3)
 
plt.xlabel("Release year")
plt.ylabel("Number of movies")
plt.title("Release year of movies I've watched")

for i in range(0, len(counted_years[0]),5):
    plt.text(counted_years[0][i], counted_years[1][i] + 0.5,
             str(counted_years[1][i]),color='crimson',fontweight='bold')
plt.grid(color = 'blue', linestyle = '--', linewidth = 0.2)
plt.show()
```


    
![png](../images/imdbanalyzer_files/imdbanalyzer_11_0.png)
    


Let's now take a look at the average ratings as a function of release year.


```python
my_avg_rating   = np.empty([len(counted_years[0])]) # Empty array
imdb_avg_rating = np.empty([len(counted_years[0])]) # Empty array

for i in range(len(counted_years[0])):
    idxs = my_movie_years == counted_years[0][i]
    my_avg_rating[i]    = np.mean(my_movie_ratings[idxs])
    imdb_avg_rating[i]  = np.mean(imdb_ratings[idxs])

avg_ratings_df = pd.DataFrame({
    'Year': counted_years[0],
    'My Average Rating': my_avg_rating,
    'IMDb Average Rating': imdb_avg_rating
})

# plotting graph
ax = avg_ratings_df.plot(x="Year", y=["My Average Rating", "IMDb Average Rating"], kind="bar", figsize=(20, 6),
        subplots=False,
        grid=True,
        color={"My Average Rating": "#002c5a", "IMDb Average Rating": "#96caff"})
ax.set_axisbelow(True)
ax.grid(color='r', linestyle='--', linewidth=0.5)
ax.grid(axis='x')

```


    
![png](../images/imdbanalyzer_files/imdbanalyzer_13_0.png)
    


Let's now see how aligned I am with the masses.

It seems that we generally agree on the 7's.


```python
plt.figure(figsize=(6, 6))
plt.scatter(my_movie_ratings, imdb_ratings, alpha=0.5, edgecolors="k")
m, b = np.polyfit(my_movie_ratings, imdb_ratings, deg=1)

# Create a sequence of 50 points from 2 to 10 
sequence_x = np.linspace(counted_ratings[0][0], counted_ratings[0][-1], num=50)

# Plot regression line
plt.plot(sequence_x, b + m * sequence_x, color="dodgerblue", linestyle = '--', lw=1.5)

# Plot y = x line
plt.plot(sequence_x, sequence_x, color="darkgoldenrod", linestyle = '--', lw=1.5)

mean_rating = np.empty([len(counted_ratings[0])]) # Empty array
std_rating  = np.empty([len(counted_ratings[0])]) # Empty array

for i in range(len(counted_ratings[0])):
    idxs = my_movie_ratings == counted_ratings[0][i]
    imdb_ratings_aux = imdb_ratings[idxs]
    mean_rating[i] = np.mean(imdb_ratings_aux)
    std_rating[i] = np.std(imdb_ratings_aux)

plt.scatter(counted_ratings[0], mean_rating, color="crimson",edgecolors="orange")
plt.errorbar(counted_ratings[0], mean_rating, std_rating, fmt="o", color="r")
plt.xlabel('My rating')
plt.ylabel('IMDb rating')
plt.title('How much do I agree with IMDb ratings?')
plt.grid(color = 'blue', linestyle = '--', linewidth = 0.2)
plt.show()
```


    
![png](../images/imdbanalyzer_files/imdbanalyzer_15_0.png)
    

