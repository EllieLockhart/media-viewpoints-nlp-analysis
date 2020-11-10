# Media-Viewpoints 
**Video Game Review Understanding Through Natural Language Processing**

Video game reviews are sites of controversy. Both reviews that are published professionally by paid critics, as well as those posted by users on sites like Metacritic, Steam, and Amazon, have generated public discourse and challenges for marketers at game studios, as well as consternation for fans. This is an issue which, at the fundamental level, extends to films, books, and music as well - but I have chosen to begin using natural language processing to better understand corpuses of video game reviews.

*The Last of Us Part II*, a Sony-published action-adventure video game sequel published in the summer of 2020, suffered leaks of major plot points, and had a contentious plotline that divided the fans of the original *Last of Us*. Metacritic, the generally-accepted primary aggregator of reviews as well as primary location for console gamers to leave reviews of the products that they consume, currently hosts over seven hundred pages of one hundred *Last of Us Part II* reviews each. This is a massive corpus of data, and much press coverage has been devoted to the "review bombing" campaign in which disingenous reviews were left, possibly by fans who had not even played the game. Despite this, the game was a commercial success. 

The extreme nature of *The Last of Us Part II*'s reception by fans (and, to a lesser degree, by professional critics) makes it an excellent "jumping off point" for natural-language based study of video game reviews in general - and the corpus of reviews is simply too large for any human to meaningfully examine in its entirety without such technology. The controversy around *The Last of Us Part II* spilled over into the Metacritic reviews of *Ghost of Tsushima*, another Playstation 4-exclusive action-adventure title released the following month. My project will begin with a comparison of the (much larger than average) corpuses of reviews of these two titles, and then expand. Some project goals include:
1. Attempt to determine what a "review bomb" negative review looks like on a structural level, and what a "sincere" review looks like (see methodology notes later in this document)
2. Determine what factors are discussed more by professional critics in official reviews and what factors are discussed more by "fans" in user reviews
3. Answer certain specific questions relating to *The Last of Us Part II* and *Ghost of Tsushima*
4. Compare and contrast professional critics' reviews published immediately upon or before the release of a game (when they may be under an "embargo" forbidding discussion of certain game elements, in exchange for advance copies) with "think pieces" posted shortly thereafter when they are no longer under such obligation (*The Last of Us Part II* also stands out, subjectively, in this sense; the release-day reviews by professional critics were *substantially* more positive and discussed substantively different issues than "think pieces"; however, deeper analysis is needed to learn exactly how and how significant this is.)

## Notes on Methodology
Using automated data collection scripts as well as a limited amount of manual data collection in specialized cases (such as identifying the aforementioed "thinkpieces"), I seek to obtain corpuses of both **user reviews** and **professional reviews** of video games. To limit the scope of the project, I intend initially to focus on action-adventure Playstation 4 exclusives, starting with a compare-and-contrast of *The Last of Us Part II* and *Ghost of Tsushima*. 

Using NLTK if possible and Tensorflow if necessary (due to the sheer size of the review corpuses), I intend to create word vector and similarity models of cleaned data and determine themes present in reviews. Utilizing a Neo4J database storage model, I will model relations of positive and negative reviews, initially using the 0-10 "metascore" awarded by users in the case of user reviews, and eventually broadening to 