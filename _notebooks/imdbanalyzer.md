Import libraries and load csv file with ratings.

The ratings file is available from your IMDb user account.


```python
import pandas as pd 
import numpy as np
import matplotlib.pyplot as plt

ratings  =  pd.read_csv("ratings.csv")
```

Parsing data.

Basically, I shall count repetitions of an instance. 

I am interested only in my own ratings, IMDb ratings, release year, and genres.

Note that one movie can have more than one genre.


```python
movie_idxs          = ratings.index[ratings['Title Type']=='movie'].tolist()

my_movie_ratings    = ratings.iloc[movie_idxs,1]
counted_ratings     = np.unique(my_movie_ratings, return_counts=True)

imdb_ratings        = ratings.iloc[movie_idxs,6]

my_movie_years      = ratings.iloc[movie_idxs,8]
counted_years       = np.unique(my_movie_years, return_counts=True)

my_movie_runtimes   = ratings.iloc[movie_idxs,7]
counted_runtimes    = np.unique(my_movie_runtimes, return_counts=True)

my_movie_genres_aux = ratings.iloc[movie_idxs,9].str.split(", ") # the space after the comma is important
my_movie_genres     = [item for sublist in my_movie_genres_aux for item in sublist]
counted_genres      = np.unique(my_movie_genres, return_counts=True)
```

Plotting the distribution of my ratings.

On top of each bar I indicate the total number of movies which I have given that score.

I guess I have not been watching too many masterpieces... 


```python
plt.figure(figsize=(10, 10))
plt.bar(counted_ratings[0], counted_ratings[1], color ='#4682B4', width = 0.5)
 
plt.xlabel("Rating")
plt.ylabel("Number of movies")
plt.title("My movie ratings")
plt.xticks(counted_ratings[0])

for i in range(len(counted_ratings[0])):
    plt.text(counted_ratings[0][i], counted_ratings[1][i] + 5,
             str(counted_ratings[1][i]))

plt.show()
```


    
![png](images/imdbanalyzer_5_0.png)
    


Plotting information about the genres.

For the sake of visualization, I will group less watched genres into *Others* and limit the pie chart to eight wedges.


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

fig, ax = plt.subplots(figsize=(10, 10))

patches, texts, pcts = ax.pie(
    genres_dataframe_compact['value'], labels=genres_dataframe_compact['Genre'].tolist(), autopct='%.1f%%',
    colors=color_shades,
    wedgeprops={'linewidth': 3.0, 'edgecolor': 'white'},
    textprops={'size': 'x-large', 'fontweight': 'bold'})

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
genres_dataframe_less_watched['#'] = [str(i + 8) for i in range(len(genres_dataframe_less_watched['Genre']))]
genres_dataframe_less_watched.set_index('#', inplace=True)
genres_dataframe_less_watched.style.set_table_styles(
    [
        {
            'selector': 'th',
            'props': [('background-color', '#D3D3D3')]
        },
        {
            'selector': 'tbody tr:nth-child(even)',
            'props': [('background-color', '#89CFF0')]
        }

    ]
)
```


    
![png](images/imdbanalyzer_7_0.png)
    





<style type="text/css">
#T_6a2ea th {
  background-color: #D3D3D3;
}
#T_6a2ea tbody tr:nth-child(even) {
  background-color: #89CFF0;
}
</style>
<table id="T_6a2ea">
  <thead>
    <tr>
      <th class="blank level0" >&nbsp;</th>
      <th id="T_6a2ea_level0_col0" class="col_heading level0 col0" >Genre</th>
      <th id="T_6a2ea_level0_col1" class="col_heading level0 col1" >Movies watched</th>
    </tr>
    <tr>
      <th class="index_name level0" >#</th>
      <th class="blank col0" >&nbsp;</th>
      <th class="blank col1" >&nbsp;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th id="T_6a2ea_level0_row0" class="row_heading level0 row0" >8</th>
      <td id="T_6a2ea_row0_col0" class="data row0 col0" >Sci-Fi</td>
      <td id="T_6a2ea_row0_col1" class="data row0 col1" >372</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row1" class="row_heading level0 row1" >9</th>
      <td id="T_6a2ea_row1_col0" class="data row1 col0" >Romance</td>
      <td id="T_6a2ea_row1_col1" class="data row1 col1" >268</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row2" class="row_heading level0 row2" >10</th>
      <td id="T_6a2ea_row2_col0" class="data row2 col0" >Fantasy</td>
      <td id="T_6a2ea_row2_col1" class="data row2 col1" >262</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row3" class="row_heading level0 row3" >11</th>
      <td id="T_6a2ea_row3_col0" class="data row3 col0" >Horror</td>
      <td id="T_6a2ea_row3_col1" class="data row3 col1" >254</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row4" class="row_heading level0 row4" >12</th>
      <td id="T_6a2ea_row4_col0" class="data row4 col0" >Family</td>
      <td id="T_6a2ea_row4_col1" class="data row4 col1" >168</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row5" class="row_heading level0 row5" >13</th>
      <td id="T_6a2ea_row5_col0" class="data row5 col0" >Biography</td>
      <td id="T_6a2ea_row5_col1" class="data row5 col1" >125</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row6" class="row_heading level0 row6" >14</th>
      <td id="T_6a2ea_row6_col0" class="data row6 col0" >Animation</td>
      <td id="T_6a2ea_row6_col1" class="data row6 col1" >109</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row7" class="row_heading level0 row7" >15</th>
      <td id="T_6a2ea_row7_col0" class="data row7 col0" >War</td>
      <td id="T_6a2ea_row7_col1" class="data row7 col1" >80</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row8" class="row_heading level0 row8" >16</th>
      <td id="T_6a2ea_row8_col0" class="data row8 col0" >History</td>
      <td id="T_6a2ea_row8_col1" class="data row8 col1" >68</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row9" class="row_heading level0 row9" >17</th>
      <td id="T_6a2ea_row9_col0" class="data row9 col0" >Western</td>
      <td id="T_6a2ea_row9_col1" class="data row9 col1" >32</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row10" class="row_heading level0 row10" >18</th>
      <td id="T_6a2ea_row10_col0" class="data row10 col0" >Sport</td>
      <td id="T_6a2ea_row10_col1" class="data row10 col1" >31</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row11" class="row_heading level0 row11" >19</th>
      <td id="T_6a2ea_row11_col0" class="data row11 col0" >Music</td>
      <td id="T_6a2ea_row11_col1" class="data row11 col1" >27</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row12" class="row_heading level0 row12" >20</th>
      <td id="T_6a2ea_row12_col0" class="data row12 col0" >Documentary</td>
      <td id="T_6a2ea_row12_col1" class="data row12 col1" >25</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row13" class="row_heading level0 row13" >21</th>
      <td id="T_6a2ea_row13_col0" class="data row13 col0" >Musical</td>
      <td id="T_6a2ea_row13_col1" class="data row13 col1" >24</td>
    </tr>
    <tr>
      <th id="T_6a2ea_level0_row14" class="row_heading level0 row14" >22</th>
      <td id="T_6a2ea_row14_col0" class="data row14 col0" >Film-Noir</td>
      <td id="T_6a2ea_row14_col1" class="data row14 col1" >15</td>
    </tr>
  </tbody>
</table>




As somewhat expected for someone born in 1990, I have been watching more movies from the recent period.

When we go to the cinema, we rarely attend sessions showing old classic movies.

Moreover, only a few classics stand the test of time.


```python
plt.figure(figsize=(10, 10))
plt.bar(counted_years[0], counted_years[1], color ='#4682B4', width = 0.5)
 
plt.xlabel("Release year")
plt.ylabel("Number of movies")
plt.title("Release year of movies I've watched")

for i in range(0, len(counted_years[0]),5):
    plt.text(counted_years[0][i], counted_years[1][i] + 0.5,
             str(counted_years[1][i]),color='red',fontweight='bold')
plt.grid(color = 'blue', linestyle = '--', linewidth = 0.2)
plt.show()
```


    
![png](images/imdbanalyzer_9_0.png)
    


Charles Bukowski once said *The masses are always wrong - Wisdom is doing everything the crowd does not do.*

Let us see how I fit his description...


```python
plt.figure(figsize=(10, 10))
plt.scatter(my_movie_ratings, imdb_ratings, alpha=0.5, edgecolors="k")
m, b = np.polyfit(my_movie_ratings, imdb_ratings, deg=1)

# Create a sequence of 50 points from 2 to 10 
sequence_x = np.linspace(counted_ratings[0][0], counted_ratings[0][-1], num=50)

# Plot regression line
plt.plot(sequence_x, b + m * sequence_x, color="r", linestyle = '--', lw=1.5)

mean_rating = np.empty([len(counted_ratings[0])]) # Empty array
std_rating  = np.empty([len(counted_ratings[0])]) # Empty array

for i in range(len(counted_ratings[0])):
    idxs = my_movie_ratings == counted_ratings[0][i]
    imdb_ratings_aux = imdb_ratings[idxs]
    mean_rating[i] = np.mean(imdb_ratings_aux)
    std_rating[i] = np.std(imdb_ratings_aux)

plt.scatter(counted_ratings[0], mean_rating, color="r",edgecolors="orange")
plt.errorbar(counted_ratings[0], mean_rating, std_rating, fmt="o", color="r")
plt.xlabel('My rating')
plt.ylabel('IMDb rating')
plt.title('How much do I agree with IMDb?')
plt.grid(color = 'blue', linestyle = '--', linewidth = 0.2)
plt.show()
```


    
![png](images/imdbanalyzer_11_0.png)
    

