# Final Project 124: Analyzing Soccer Predictions

## By Arianna Velasco

Original [CSV Table](https://projects.fivethirtyeight.com/soccer-api/club/spi_matches.csv)


The CSV file had a lot of leagues including second division teams. However I wanted to look at the teams from first-division teams in Europe as well as the EUFA Champions Europa League.

These Leagues and their id's are
* French Ligue 1-1843
* Barclays Premier League-2411
* Spanish Primera Division-1869
* Italy Serie A-1854
* German Bundesliga-1845
* Austrian T-Mobile League-1827
* Belgian Jupiler League-1832
* Danish SAS-Ligaen-1837
* Dutch Eredivisie-1849
* Norweigan Tippeligaen-1859
* Portuguese Liga-1864
* Russian Premier Liga-1866
* Greek Super League-1884
* Swedish Allsvenskan-1874
* Scottish Premiership-2417
* Swiss Raiffeisen Super League-1879
* Turkish Turkcell Super Lig-1882
* UEFA Champions League-1818
* UEFA Europa league-1820

In order to get all of these I placed the filter on the sheet and selected all of the leagues shown above. 

The Data also held the data on different season which run from Fall to Spring of next year.

* 2016-2017
* 2017-2018
* 2018-2019
* 2019-2020
* 2020-2021


### Warmup

To get myself accostumed to the data I decided to run a couple of tests with all of the data of European Legues throughout the 5 seasons presented. 

One of The first things that I wanted to discover what match had the most goals in all of Europe.

To get this information I created a new pillar named "Game with Highest Goals" with a sum formula.

```
SUM=(Q1,R2)
```
I then made the column give me the highest value. 

To get a closer look at the goal statistics I created a pivot table that the total number of goals scored in the leagues (this excluded the Champions and Europa Legue), the average and the Max in one game. 

*Table with all of the values*

![Table](https://media.journalism.berkeley.edu/upload/2020/08/1597090236ca9f254.png)

This was the result for the total goals in the leagues through the seasons 2016-2020

<iframe title="[ Total Goals in league from 2016 to 2020 Season]" aria-label="map" id="datawrapper-chart-aGLUD" src="https://datawrapper.dwcdn.net/aGLUD/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="583"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

*Not Russia could not be added but the total number of goals was 1654

*Note Every league had a diffrent amount of games accounted for in the season so this is not the best way to see who had the most goals. So I decided to get the averages.

This was the result for the avearge goals per game in the leagues through seasons 2016-2020.

<iframe title="[ Average Goals in league from 2016 to 2020 Season]" aria-label="map" id="datawrapper-chart-aGLUD" src="https://datawrapper.dwcdn.net/aGLUD/2/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="583"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>

*Note Russia could not be added but they had an average 2.29 goals per game

This was the result for the maximum goals scored in one game through seasons 2016-2020

<iframe title="[Max Number of Goals in a Single Match  2016-2020]" aria-label="map" id="datawrapper-chart-BLWwC" src="https://datawrapper.dwcdn.net/BLWwC/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="583"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>


*Note Russia could not be added but they had the maximum gaols in a single match with 11 



With this data we have a better Idea of the Goal Data among the European League throughout the 5 seasons. However its importnat to note that not all of the leagues were accounted for every year. So the Sum of leagues is not the best Data. From all the games documented in each league for the 5 seasons (if the legue is recorded) the goal average per game is shown in the data. And from all of the games documented during the 5 seasons the highest score was 11 goals. 

### Italia Seria A Stats

#### WHO IS THE LEADER

Now I want to look closely at a single ligue - I decided to choose the Italia Serie A league.

They have seasons 2016 to 2019 but i will be looking at season 2019-2020

First i wanted to see who were the stronger teams right off the bat. To do that SPI which stands for the teams overall strength it was coming with during the match. I decided to do SPI1 first.

Juventus had the highest SPI1 by Far.

![Table](https://media.journalism.berkeley.edu/upload/2020/08/1597185581ad79928.png)

The other two that followed in the column were Napoli and Atlanta.

I did the same and not suprisingly the table looked the same as it did for SPI2

I then looked at column Prob 1 which is the probablity that team 1 would win. I expected to see Juventus on top since based on what we saw before it is the strongest team in the league.

![Table](https://media.journalism.berkeley.edu/upload/2020/08/1597186399fdf048f.png)

*I look at the top 20 spots

The result is similar to the tables before however we see more of Atlanta and Napoli as well as Internazionale. However What I found out when looking at the Team 2 column is that the a couple teams showed up at least more than two times.

* Verona
* Brescia
* Spal
* Genoa
* Lecce
* Cagliari

Based on this information I presumed that if we did the probablity from Team 2 it would look similar. When I tried it again it was very similar with Juventus on top followed by Internazionale, Atlanta, and Napoli. This time the teams Lazio and AS Roma showed up. 

On Team 1 I saw the same teams listed above showed up as well, however this time Parma took the top spot. 
Seeing these results I wanted to test out a theory. I believed that the teams 

* Verona
* Brescia
* Spal
* Genoa
* Lecce
* Calagari 
* Parma

have the lowest SPI in the league. In other words they are the worst teams in the league.
To test this I went to SPI 1 and organized it from worst to best

This was the result 

![Table](https://media.journalism.berkeley.edu/upload/2020/08/15971875371e764d9.png)


Turns out that the team with te worst SPI was Brescia, followed by Lecce and Spal. All three show up on the table below. If we continue to scroll down the other teams named also start to show up. 
While there is no correlation from looking at the highest probablity of a team winning, if you look at the teams they will be up against we can get an idea of the worst teams in the league. 

Gping abck to Juventus I wanted to see the probabilities the team had against winning against other Teams,
I looked at Juventus probablities as Team 2.



Round2/Team2


<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRiC-ACgKMoP_F_s6G4qsrEmg-ztZTvMurcPJRWOP_D5F4-U_1n0mONvhlkkZnyQYtuXKDXm3DHUxTP/pubchart?oid=610888918&amp;format=interactive"></iframe>


What can be seen from the graph is that teams that have lower SPI give Juventus a higher probablity while the teams with higher SPI give Juventus a lower chance of winning. 

So what can we take out of this data analysis. 

* Juventus is the strongest team fllowed by Atlanta and Napoli according to SPI stats
* Brescia is the lesser team followed by Lecce and Spal according to SPI stats
* The Lower the SPI the easier for Juventus to defeat the higher the SPI the possibilities of winning for Juventus go down.


To see how the data worked with the actual result here is the final legue result. 

[TABLE 2019/202](https://www.skysports.com/serie-a-table)

From the result we can see that Juventus was first place, and Atlanta came in at third, however Napoli came in at 7. Brescia came in second to last after Spal however they along with lecce were in the bottom 3.




### Champions League

Now I will be analyzing the Champions League of 2019/2020. 

First I want to see what League has the highest SPI for the 2019-2020

#### Best League

So basically we know that the higher the SPI the team has the better it is prepared before the match. So  The higher the SPI is in the league the better/competive the league is becasue it has better prepared teams. 

I created a pivot table which gave me the average of SPI 1 and SPI 2. However I wanted to get the overall SPI of the league.

*Note In leagues teams have home and away games which stand for Team 1 and Team 2. So SPI 1 only take sin account the games played in the first match. That is why they must be united. However the SPI is almost identical on both since they are the same teams and not many major changes happen within the season. 

So I made the Formula 

```
Sum(B1,C2)/2
```

The result was:

![Table](https://media.journalism.berkeley.edu/upload/2020/08/15972073395107cfa.png)

England had the highest overall SPI with 74.38

*Note this does not mean that England has the best team. They could have multiple 80 SPI team while Spain has a 90 SPI but teams with a lower SPI that reduce the average lower than Englands. 

<iframe title="[ Average SPI per League ]" aria-label="map" id="datawrapper-chart-10gKL" src="https://datawrapper.dwcdn.net/10gKL/1/" scrolling="no" frameborder="0" style="width: 0; min-width: 100% !important; border: none;" height="583"></iframe><script type="text/javascript">!function(){"use strict";window.addEventListener("message",(function(a){if(void 0!==a.data["datawrapper-height"])for(var e in a.data["datawrapper-height"]){var t=document.getElementById("datawrapper-chart-"+e)||document.querySelector("iframe[src*='"+e+"']");t&&(t.style.height=a.data["datawrapper-height"][e]+"px")}}))}();
</script>


Now Back to the Champions League.

*Note due to COVID-19 the Final results of season 2019-2020 have not been finalized

First i want to see if the Champions league is holding up to its standards.

I followed the same process I did for the league except the only Row I made for my Pivot Table was UEFA Champions League.

As expected the Total was higher = 79

Therefore Champions league has better prepared teams than any of the other Leagues based on their SPI score. This of course is expected since only the highest ranking teams from each league qualify to go to the Champions league.

#### Who will win?

Becasuse of COVID-19 THe Champions League tournament had to shutdown in march and started back up in August. 
Last week they finished The first round of eliminations. 
And based on all my exploration in this project I want to make a guess on who has the most chances of winning. 

First I will organize the table in a chronological order.

In the next for days the quarter finals will take place. 

There are currently 8 teams and their latest SP1:

* Atlanta 82.56
* RB Leipzig 85.75
* Barcelona 90.54
* Manchester City 95.59
* Paris Saint-Germaine 89.15
* Atletico Madrid 85.54
* Bayern Munich 94.42
* Lyon 72.9

*note values are rounded
The Next Matches are:

Paris Saint-Germaine vs Atlanta with a 37% chance of victory for Atlanta and 63% for Paris 
RB Leipzig vs Atletico Madrid with a 52% chance of victory for Leipzig and 48% for A.Madrid
Barcelona vs Bayern Munich with a 39% for Barcelona and  61% for Bayern Munich\
Manchester city. vs Lyon with a 89% chance of victory for Manchester city and 11% for Lyon

Here are my predictions based on the Data:

##### SemiFinals
Paris Saint Germaine vs RB Leipzig

Bayern Munich vs Manchester City

##### Finals

Paris Saint Germaine vs Manchester City

##### Winner

Manchester City

Keep in mind that these are predictions based on prerecorded stats but anything can happen. 

### GO BARCELONA




