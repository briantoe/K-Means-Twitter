# How to execute this program. 
1. Ensure that Python3.6 or later is installed locally.
2. Install dependencies, run `python -m pip install -r requirements.txt`
3. Run `python hw_kmeans.py` with the data file `cbchealth.txt` in the same directory.

# Libraries used
1. numpy
2. collections
3. copy
4. re, the regular expressions library

# Purpose
Twitter provides a service for posting short messages. In practice, many of the tweets are very
similar to each other and can be clustered together. By clustering similar tweets together, we can
generate a more concise and organized representation of the raw tweets, which will be very
useful for many Twitter-based applications (e.g., truth discovery, trend analysis, search ranking,
etc.)

This program uses Jaccard Distance to compute distances between cluster centroids.

Jaccard Distance Dist(A, B) between tweet A and B has the following properties:
  - It is small if tweet A and B are similar.
  - It is large if they are not similar.
  - It is 0 if they are the same.
  - It is 1 if they are completely different (i.e., no overlapping words).
  
Here is the reference for more details about Jaccard Distance:
http://en.wikipedia.org/wiki/Jaccard_index

Hint: Note that since the tweets do not have numerical coordinates as in Euclidean space, you
might want to think of a sensible way to compute the "centroid" of a tweet cluster. This could be
the tweet having minimum distance to all of the other tweets in a cluster
