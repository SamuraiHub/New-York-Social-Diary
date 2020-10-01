# New-York-Social-Diary
A data analysis project done by web scraping the New York Social Diary for its photo captions. The goal of this project is to uniquely count all the people captioned in the New York Social Diary.

New York Social Diary provides a fascinating insight into the life of New York's social elite. The data forms a natural social graph. Take a look at this page of a recent run-of-the-mill holiday party:

http://www.newyorksocialdiary.com/party-pictures/2014/holiday-dinners-and-doers

You will notice the photos have carefully annotated captions labeling those that appear in the photos. We can think of this as implicitly implying a social graph: there is a connection between two individuals if they appear in a picture together.

## The project was implemented as follows:

The first step is to crawl the data. We want photos from parties before December 1st, 2014. Go to http://www.newyorksocialdiary.com/party-pictures to see a list of (party) pages. For each party's page, grab all the captions.

## The second step is to answer these questions

### 1. degree
The simplest question to ask is "who is the most popular"? The easiest way to answer this question is to look at how many connections everyone has. Return the top 100 people and their degree. Remember that if an edge of the graph has weight 2, it counts for 2 in the degree.

### 2. pagerank
A similar way to determine popularity is to look at their pagerank. Pagerank is used for web ranking and was originally patented by Google and is essentially the stationary distribution of a markov chain implied by the social graph.

Use 0.85 as the damping parameter so that there is a 15% chance of jumping to another vertex at random.

### 3. best_friends
Another interesting question is who tend to co-occur with each other. Give us the 100 edges with the highest weights.

Google these people and see what their connection is. Can we use this to detect instances of infidelity?

The first file (NewYorkSocialDiary.ipynb) is where the project was implemented while the second file is just an html version of the first file.
