# Anime recomendation system

## Preprocessing

### user_history.py

- Select only users who have seen between 100 and 1000 animes, any fewer, any more is eliminated. Most users lie within this range so we are able to reserve most of the data and remove noise or irrelevant data. Saved in `user_anime_dict={user_id:[list of anime id]}`

- Select only animes that have been seen by those users. Saved in `anime_num_users_dict = {anime_id:number_of_users}`

### anime_list.py

Select only animes that appears in the above list. Save in the list `anime_list_dict = [{anime_id:str, name:str, type:str, episodes:float, rating:float, members:float, genre = [], num_viewers:int}]`

### genre_onehot.py

Get unique genres and save in `genre_list = []`

Get manga ids and save them in `id_list = []`

Get onehot encoded vector of id - genre (index is ordered according to the 2 lists above) and save in `id_genre = [[],[],...]}`

## Clustering

For each user, see if their user history mostly contains anime from which cluster.
Recommend the ones in the same cluster with highest viewers... that the user hasnt viewd.
Recommend the ones in the n closest clusters and recommend the highest rated/closest points in those.

Scalability: group users that have the same taste -> rec to all of them => onehot based on anime clusters => use GMM => sort prob of someone in same cluster

Test:

separate each user's history into 80/20

recommend some based on 80 -> compare with 20

stratified => equal classes


