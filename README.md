# Movie Critics Recommender System
A movie critics recommender system implemented in python that uses 3 similarity measures:

1. Pearson Correlation Coefficient
2. Tanimoto similarity
3. Euclidean Distance
## Usage
The following code can be used to get the recommended movies for a critic using the different similarity measures:


critics={'Lisa Rose': {'Lady in the Water': 2.5, 'Snakes on a Plane': 3.5,
 'Just My Luck': 3.0, 'Superman Returns': 3.5, 'You, Me and Dupree': 2.5, 
 'The Night Listener': 3.0},
'Gene Seymour': {'Lady in the Water': 3.0, 'Snakes on a Plane': 3.5, 
 'Just My Luck': 1.5, 'Superman Returns': 5.0, 'The Night Listener': 3.0, 
 'You, Me and Dupree': 3.5}, 
'Michael Phillips': {'Lady in the Water': 2.5, 'Snakes on a Plane': 3.0,
 'Superman Returns': 3.5, 'The Night Listener': 4.0},
'Claudia Puig': {'Snakes on a Plane': 3.5, 'Just My Luck': 3.0,
 'The Night Listener': 4.5, 'Superman Returns': 4.0, 
 'You, Me and Dupree': 2.5},
'Mick LaSalle': {'Lady in the Water': 3.0, 'Snakes on a Plane': 4.0, 
 'Just My Luck': 2.0, 'Superman Returns': 3.0, 'The Night Listener': 3.0,
 'You, Me and Dupree': 2.0}, 
'Jack Matthews': {'Lady in the Water': 3.0, 'Snakes on a Plane': 4.0,
 'The Night Listener': 3.0, 'Superman Returns': 5.0, 'You, Me and Dupree': 3.5},
'Toby': {'Snakes on a Plane':4.5,'You, Me and Dupree':1.0,'Superman Returns':4.0}}

#Using Euclidean Distance
print(topMatches(critics, 'Toby', n=3, similarity=sim_distance))
#Output: [('Mick LaSalle', 0.4721359549995794), ('Lisa Rose', 0.41421356237309503), ('Jack Matthews', 0.4035668847618199)]

#Using Tanimoto similarity
print(topMatches(critics, 'Toby', n=3, similarity=sim_tanimoto))
#Output: [('Mick LaSalle', 0.6666666666666666), ('Lisa Rose', 0.5714285714285714), ('Jack Matthews', 0.5000000000000001)]

#Using Pearson Correlation Coefficient
print(topMatches(critics, 'Toby', n=3, similarity=sim_pearson))
#Output: [('Jack Matthews', 0.9912407071619299), ('Mick LaSalle', 0.9244734516419049), ('Lisa Rose', 0.8934051474415647)]


## Contributing
1. Fork it
2. Create your feature branch (`git checkout -b
