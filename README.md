# Football_Analytics

Alright, alright alright! This project focuses on college football, and analyzing some data that was scraped with code in this  <a href="https://github.com/havelljd/Football_Scraping">repository,</a>. The data used for this project is described more in-depth on that repo, but in short, I've scraped roughly 70 college football teams offensive stats and records for each season from 2007-2022. That data was dumped into a .csv file to avoid having to scrape for 2-3 hours to get the data (if needed, I could bring that code into this repo to always have up to date data). The .csv file is hosted by a cloud provider for easy access.

To get this project started, I brought the scraped data into a pandas dataframe. Then I cleaned up a sinlge column of data from this

<img width="68" alt="image" src="https://user-images.githubusercontent.com/8563653/210691533-f9c67ad8-dc56-46e3-86d2-98083c8f0892.png">

to this

<img width="320" alt="image" src="https://user-images.githubusercontent.com/8563653/210691598-64cc0d8e-3eb4-494d-bfbb-31047e515dfb.png">

just to split out the result of a game and the scores of each team (the web scraper placed them into the same column).

After that, I had the data how I wanted it. I proceeded to visualize some of the data in bar chart format, grouping wins and losses recorded by teams into conference wins and losses.

<img width="645" alt="image" src="https://user-images.githubusercontent.com/8563653/210692977-788fb55a-b84d-4083-be44-519c48167dcf.png">

However, this included some non 'Power 5' conferences. Power 5 conferences are the 5 biggest college football conferences, and this project was only meant to target those schools. So why are there more than 5 conference included in the data? It had to do with previous schools joining different conferences; for example, in 2007, both BYU and Utah were in the Mountain West Conference, but in 2022, BYU was independent (joining the Big 12 conference in 2023) and Utah was in the Pac-12 conference. Because I know which teams got sorted into which conference, I had to go in and update the data to reflect that. Here are the teams that moved up into the current Power 5 conferences:

<img width="145" alt="image" src="https://user-images.githubusercontent.com/8563653/210693665-1fc8fbde-f240-49af-90ce-1e94b117b89d.png">

After sorting their wins into their current (and future) conferences, the updated bar chart looked like this (I kept Ind conference, as Notre Dame doesn't belong to any Power 5 conference but is still considered a "major" team):

<img width="632" alt="image" src="https://user-images.githubusercontent.com/8563653/210694621-45b262f8-0854-4de6-9b2f-9b86ef65d0b3.png">

I'm planning to do more visualizations on this data; I think a scatterplot of school wins across the past 15 seasons overlaid with touchdowns scored, and yards per game.

After that, I ran some regression models to predict wins based on the features in the dataframe. This section is not completed yet, and will be updated soon with more accurate and explainable models to predict wins for football teams!
