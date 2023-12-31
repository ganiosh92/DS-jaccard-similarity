# DS-Jaccard-similarity
code to compute Jaccard's distance to compare similarity between two items based on 'n' attributes

# So what is Jaccard Similarity and why do we need it?
There are often times when we would like to compare two things based on their non-numeric characteristics. Like two shirts that have different colors or patterns or two destinations that offer same or different types of visitor entertainment. We come across cases like that mostly in Machine Learning.

So the question is how do we go about making these comparisons? The answer lies in a measure called Jaccard Distance. Jaccard distance helps us compare two things based on the information we about their categorical attributes.

# Example
For example, if we have two locations L1 and L2 and the activities they offer are as follows:

- L1 - {Hiking, Skiing, Swimming, Shopping}
- L2 - {Hiking, Shopping, Scuba-Diving, luxury-dining}

Then we calculate the Jaccard Similarity between L1 and L2 by calculating the number of items in the intersection of L1 & L2 and then dividing that number by the number of unique items in the union of L1 and L2.

- L1 ∩ L2 = {Hiking, Shopping} => n(L1 ∩ L2) = 2
- L1 ∪ L2 = {Hiking, Skiing, Swimming, Shopping, Scuba-Diving, Luxury-Dining} => n(L1 ∪ L2) = 6
- Jaccard Similarity = n(L1 ∩ L2) / n(L1 ∪ L2) = 1/3 ~ 0.33
- Jaccard Distance = 1 - (Jaccard Similarity) = 0.67

So, we can conclude by saying that Locations L1 and L2 are not that similar. But that is not enough because how else do we interpret a Jaccard Similarity of 0.33? Well, here's the thing Jaccard distance is more useful when it is used to compare the an item to more than or equal to two items. In this case it would be another location L3 which has a certain set of activities as well:

- L3 - {Haunted House, Skiing, Swimming, Shopping, Jazz}
- L1 ∩ L3 = {Skiing, Swimming, Shopping} => n(L1 ∩ L3) = 3
- L1 ∪ L3 = {Hiking, Skiing, Swimming, Shopping, Haunted-House, Jazz} => n(L1 ∪ L3) = 6
- Jaccard Similarity = n(L1 ∩ L3) / n(L1 ∪ L3) = 1/2 ~ 0.50
- Jaccard Distance = 1 - (Jaccard Similarity) = 0.50

Now the Jaccard Distance makes more sense. We know that in terms of similarity location L1 is closer to location L3 compared to location L2 (Jaccard distances for L3 and L2 are 0.50 and 0.67 respectively)
