# The analysis tasks

The data is in the `movielens/` folder. Read `movielens/README.txt` before you write anything. It
describes how the data was collected, and at least one of the tasks below means something
different once you have read it.

## Task 1. Highest rated movies

Which movies have the highest average rating, counting only movies with at least 50 ratings?
Report the top 10 movies.

## Task 2. Broadest taste

Which users rated movies from the largest number of different genres, counting only users who
rated 25 or fewer movies? Report the top 3 users.

A single movie can belong to more than one genre. That is what makes this harder than it looks.

## Task 3. User pairs with shared viewing habits

Which pairs of users had the highest overlap in the movies they rated? Report the top 5 pairs.

First compute this in a naive way, as the pairs with the highest count of movies that both of them
rated.

Then write a little explanation of why this might provide an uninteresting result. (Hint: think
about a pair of users with very niche tastes, but the same niche; will this approach surface that
pair?)

Finally, propose an alternative measure of "overlap", implement that, and see whether you get the
same pairs that you got from the naive approach.
