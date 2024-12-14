Gracie Maulik and Carly Martin  
December 5, 2024  
[Link to CoLab worksheet](https://github.com/carfinkle/WNBAPlayingTime/blob/main/Data_Science_Final_Project_Code.ipynb)

# Introduction

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; This analysis attempts to examine the relationship between regular-season playing time distributions and final rankings of WNBA teams. The goal is to determine if there is a specific method of determining playing time that is the most successful. Do successful teams only play their best players the majority of the game, or do they utilize their entire bench and evenly distribute the load? The aim is to determine and identify if any successful playing time patterns exist while providing the proper visualizations.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The data used in this project is taken from the WNBA Statistics page[^1], the official website for all of the league’s statistics. Data was taken from the past 5 seasons (2020-2024) which required constructing a new dataset from existing sets. The original data was sorted by individual season and included each player's average per-game statistics. To begin, each of the 5 sets of regular season and playoff data were downloaded and added to a separate sheet in an Excel workbook. From there, individual data frames were created in Google Colaboratory. To each data frame, we added a column for the respective year which proved helpful later when the datasets were merged. The next step was to incorporate the rankings that each player’s respective team earned at the end of that season. Using data from ESPN[^2],  the final team rankings were added to each dataset for each player. The data frames were then merged leaving us with one large dataset including entries from 2020 to 2024\. Finally, the columns that contained irrelevant  variables for the analysis were removed in order to keep the set workable and clean. The process was repeated for playoff data.   

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Secondly, we examined the distributions of average playing time per game for each team across 5 years to see if there were detectable, successful patterns both during the regular season and playoffs. Each WNBA team’s resulting five distributions were examined, representing each of the last five seasons. Each graph has average playing time on the x-axis and density on the y-axis. The density represents the frequency with which a playing time was observed among players in the team. The final ranking of the team was included along with commentary on any patterns observed. Additionally, the playoff distributions for the teams who eventually won the championship are explored. Finally, distributions were created for the 5 teams who finished first, last, and became champions in each of the last five seasons and examined for patterns.

# Methods and Results: Individual Teams

### *Atlanta Dream:*  

{% include_relative figures/ATL.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The Atlanta Dream changed its strategy drastically from 2020 to 2021, going from a flatter distribution and utilizing stronger players more to uniform time for everyone. This did not help their ranking in those seasons, as they went from 10th to 11th. 2022 also saw fairly even playing time amongst all players and a return to 10th place. In 2023 and 2024, the distribution shifts to peak below 20 minutes and become wider, indicating that the majority of players saw less than half of the game, but some outliers had higher playing amounts. Their ranking increased in these years as well, to 5th and 8th.  

### *Chicago Sky:*  

{% include_relative figures/CHI.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;	The Chicago Sky have seen their fair share of success throughout the last five years. Their playing time distributions for the regular season between their best season (2022) and their worst season (2024) are quite different. The distribution of playing time in 2022 was bimodal with peaks in minutes around 28 and 10 minutes. This indicates a mix of traditional “star” players who are on the floor for more minutes at a time and “role/bench”  players who act more as support players. In this year, the Sky appeared to rely more on their star players as that peak is higher than that of the role players. This could indicate a lack of trust in the bench or the high caliber play from the team's best players. In 2024, their worst season as of late, the Sky played more players and gave out fewer minutes to in the process. This could indicate a rebuilding year for the team. The Sky could be trying to foster more players at once and get them more experience. In fact, the Sky received two first round draft picks in Angel Reese and Kamilla Cardoso in 2024[^3] and the distribution of playing time alludes to the potential strategy to foster the chemistry and experience in this young team. The average number of minutes played per game that year was 18.19.   

{% include_relative figures/CHIpf.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; However, Chicago’s best playoff run was in 2021, the team entered the playoffs as the 6th seed and came out with a championship. Their distribution in playing time from the regular season into the playoffs saw a dramatic shift. The team went from a narrow single-peaked distribution to a more uniform, bimodal distribution. The number of minutes played 25th percentile in the regular season was 11.9 compared to the 25th percentile in the playoffs’ 7.4. Similarly the 75th percentile of playing time in the regular season was 26.2 compared to 32.55 in the playoffs.  The Sky changed their strategy entering the playoffs and relied proportionally on their star and bench players. Their stars consistently played around 25-30 minutes compared to the bench’s 5-10 minutes. The bimodal shape of the distribution also reflects the consistency of playing time among the players.   

### *Connecticut Sun:*  

{% include_relative figures/CON.html %} 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The Connecticut Sun finished with their worst ranking in the past 5 years in 2020 at 7th. The distribution was bell-shaped and peaked around 15 minutes. The next 4 years show multiple peaks, with the highest around 30 minutes and the lower peak less than 10 minutes. This shows that there is unequal playing time on this team with some people playing close to full games and others barely leaving the bench. This strategy appears to work for the Sun as they entered the playoffs in first place in 2021 and have placed 3rd in the years since.  

### *Dallas Wings:*

{% include_relative figures/DAL.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The distribution of playing time in 2020 was incredibly steep and peaked around 20 minutes, indicating that most players saw half of the game. The team finished 9th this year, showing it might not be a great strategy. The distributions continually get flatter as years go on, indicating that some players are seeing higher average playing times and others are seeing lower averages. From 2021 to 2023, the Wings increased their ranking each year, only to fall to 11th in 2024\.  

### *Indiana Fever:*

{% include_relative figures/IND.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The 2024 WNBA season saw the Indiana Fever have their best performance in recent years. The team ended the regular season in 6th place and made the playoffs for the first time in eight years. Their best season had their athletes playing an average of 19.44 minutes and showed a narrow unimodal distribution. This showcases the organization’s strategy of having their players play a similar amount of time. They only have a few players who average more than 19.44 minutes and only a few who average less. The distribution shows less distinguishable groupings than other teams.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; However, this does not appear to be a new tactic for the Fever. 2024 had a similar distribution of playing time compared to previous seasons indicating a growth in chemistry and ability to work together as a team. There were no drastic changes in terms of playing time thus indicating that there must have been a change in the caliber of players the fever brought in and/or the cohesion of the team on the court.   

### *Las Vegas Aces:*  

{% include_relative figures/LVA.html %} 
	
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The Aces have been one of the premier teams in the WNBA over the last few years finishing the regular season in first place three of the last five years. Their worst performance in recent years was in 2024 in which they finished the regular season in fourth place. During this time, they had fewer players who played large minutes and more who played fewer minutes. Their 2024 distribution was also one of their widest. It has the largest standard deviation of the Aces last five seasons at 12.023667 minutes. This could indicate a lack of consistency in minutes played or the coach’s want to extend minutes to her bench players and provide them with valuable experience. A wide range of playing times could also indicate injuries and the coaches attempt to fill the gaps of those players.    

{% include_relative figures/LVApf.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; That said, the Aces have won two championships in the last three years. Both years, in the playoffs, they had bimodal distributions. This again alludes to the strategy of playing the star players the majority of the game while sprinkling in role players to provide invaluable support. The bimodal distribution again implies that the coaches are consistent with the amount of minutes they hand out to each player. In 2020 and 2021, where they finished the regular season first and second respectively. However, the Aces did not come away with a championship either year (in 2021 they didn’t even make the title game) and their playoff playing time distributions are drastically different than when they did. Both years have extremely narrow distributions, with standard deviations of 10.278946 and 10.195882 respectively, and are unimodal distributions. This indicates that the Aces either relied too heavily on their star players and did not have the bench support necessary to win a championship or played their star players and bench players a similar amount, not effectively utilizing the weapons at their disposal.    

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Las Vegas also didn’t win the championship in 2024 but did employ the same bimodal distribution of playing time as their previous, championship seasons. However, the Aces did enter the playoffs as the four seed. This could indicate the possible lack of cohesion in the regular season carrying over to the playoffs. Additionally, between 2023 and 2024, the team lost two-time league MVP and starter Candace Parker to retirement/injury[^4] leaving the team to fill the massive void she left. So while the bimodal playing time distribution proved very effective in 2022 and 2023, it didn’t translate to championship success in 2024\.   

### *Los Angeles Sparks:*  

{% include_relative figures/LAS.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Above is the Los Angeles Sparks playing time distribution over the past 5 seasons. Also included is the final ranking the team finished at the end of each year. The Sparks had incredibly similar distributions in 2021 and 2023, but they finished near the bottom in both years. The team had a more uniform distribution in 2022 and 2024 but finished second-to-last and last in those years respectively. The only year they finished well was in 2020 where they finished 3rd. The distribution is uniform and peaks at lower average minutes than the rest of the distributions, indicating that the playing time was uniform on the team and that they relied more on their bench and subbed consistently.  

### *Minnesota Lynx:*  

{% include_relative figures/MIN.html %} 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The Minnesota Lynx are a historically good WNBA franchise and have made the playoffs four of the last five years. They also appear to have some of the most consistent distributions of playing time among WNBA teams in the last five years. All distributions are narrow and have one distinct peak. Excluding 2022, the average number of minutes per game played ranged from 18.16to 19.46 and the standard deviation ranged from 8.74 to 10.79 minutes per game. The 2022 season has the highest peak of all Lynx distributions at around 15 minutes per game. The Lynx therefore had more players playing fewer minutes than stars playing large minutes. This is to be expected because in 2022, the Lynx’s best player,  Napheesa Collier, who finished second in the MVP race in 2024, missed the majority of the season due to maternity leave[^5]. Therefore the Lynx had to adjust to her absence, playing more role players around 10-20 minutes a game. This rotation of players only playing 15 minutes a game may not allow them to “get their footing” and feel comfortable within lineups. The combination of this and the absence of their best player lead to the worst Lynx finish in the last five years: ending the season in ninth place and missing the playoffs all together.   

### *New York Liberty:*  

{% include_relative figures/NYL.html %} 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; New York in 2020, 2021 and 2022 were consistently finishing towards the bottom of the rankings, 12th (last), 8th, and 7th respectively. Each of the corresponding regular season distributions are quite narrow and with peaks closer to 20-30 minutes a game. In 2020 especially, the highest peak was around 25 minutes a game. The average number of minutes played per game in 2020, 2021 and 2022 were 20.26, 21.65 and 20.25 respectively. Additionally, their respective standard deviations were 6.44, 7.76 and 7.72. This is a strong indication that the liberty relied heavily on a few players to take most of the minutes.   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; However, they saw success in 2023 and 2024, finishing the season in 2nd and 1st respectively. These distributions are drastically different from the three previous. They are much wider with standard deviations of 11.101061 and 10.619108 respectively. Both the 2023 and 2024 were much more uniform, indicating that the team had some star players mixed in with a healthy amount of role players. Additionally, they relied on them equally and consistently. 

{% include_relative figures/NYLpf.html %}
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; In both 2023 and 2024, the New York Liberty made it to the championship game, winning it in 2024\. While their regular season distributions were quite uniform, their successful playoff distributions were again bimodal. During their title run, the liberty consistently played their star players more minutes while sprinkling in their role players. They relied equally on both groups with their stars consistently playing 25-45 (higher than 40 because two of the games went into overtime) and bench players playing 5-15 minutes per game.   

### *Phoenix Mercury:*

{% include_relative figures/PHO.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; In 2020, the Phoenix Mercury had a high distribution of players averaging around 20 minutes per game where they finished 5th. In 2021, they also finished 5th, but with a much flatter distribution and utilizing longer playing time for some players. 2022, 2023, and 2024 all have two peaks, one around 10 minutes and one around 30 minutes, indicating that players either played most of the game or a small part. Few played about half of the game. Their ranking decreased as this pattern started, finishing in 8th, 12th, and 7th place in the past three years.  

### *Seattle Storm:*  

{% include_relative figures/SEA.html %} 

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The Seattle Storm do not follow consistent patterns in their playing time distributions. In 2020, they finished 2nd and had a very narrow distribution around 20 minutes. In 2021, they had a much wider distribution, indicating more variation in playing time. In 2022, they had significant peaks around 30 minutes and a narrower distribution once again. In 2023, they follow more of the pattern from 2021, which saw them their worst ranking by far in the last 5 years. Finally, in 2024, the distribution is much flatter and spread out, indicating players had different playing time averages all across the team.  

{% include_relative figures/SEApf.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The storm won the championship in 2020 when they entered the playoffs as the two seed. During their successful 2020 run, they had a large number of players playing around 5-15 minutes per game with fewer playing between 20 and 35 minutes. Additionally, in 2020, their regular season distribution did not change much in shape when the team entered the playoffs. This is most likely due to how the 2020 season was structured. The COVID-19 pandemic was running rampant during this time and therefore, the 2020 WNBA season was a condensed and isolated season. Instead of the normal 40 regular season games, the 2020 “Bubble” season was only 20 games[^6]. Because there were less games played in the regular seasons, teams did not need to manage the workload of their star players as much as they would in a season that is double in length. This meant that their lineups could be more consistent in playing time because there was less concern for long-term fatigue. Therefore, the distributions of the regular season and playoffs look more similar to each other than other seasons. 

### *Washington Mystics:*  

{% include_relative figures/WAS.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Over the last five seasons the Washington Mystics have had average at best regular seasons. There is not much consistency among their distributions. Most of them are unimodal with the exception of 2020\. 2024 saw their highest peak indicating not much variation in the number of minutes each player plays per game.The 2021 season has an almost symmetrical distribution heavily implying that the team did not rely on any star players and instead played many players an average amount of minutes per game. Their best regular season finish was fifth place in 2022\. During this year, the distribution was right skewed indicating that they had some players playing large minutes while most played around ten per game.

# Methods and Results: Top and Bottom-Ranked Teams, Championship Teams

### *Twelfth-Ranked Teams:*  

{% include_relative figures/Twelve.html %}

 &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; In the past 5 years, there have been many different distributions of average playing times by teams who ranked last at the end of the season.  In 2020, the New York Liberty had a high density of players who played between 25 and 30 minutes per game, on average, with another small group sitting around the 15-minute range. In 2021, the Indiana Fever finished last with a very even distribution of playing time, with a normal curve centered right around 20 minutes per game. In 2022, the Fever also finished last, but they switched up their strategy. The distribution shifted to peak around the 15-minute mark and had a small hump around 30 minutes. This indicates that they relied heavily on a few players to be in the game, but it was not successful. The 2023 Phoenix Mercury had two sets of players, those who played less than 10 minutes on average and those who played around 30 on average. They relied on a few to do the heavy lifting on the season and that strategy did not result in many wins. Finally, in 2024, the Los Angeles Sparks had fairly even playing time, evenly distributed around 20 minutes, but it did not pay off for them in the end. Overall, there is no clear pattern of playing time distribution for teams who ranked last in the past 5 seasons. Some teams used the entirety of their bench, and some teams relied on their strongest players to do the work, but all of them have room for improvement in the coming years.  

### *First-Ranked Teams:*  

{% include_relative figures/One.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The teams that finished the regular season in first place have also had somewhat similar distributions of playing time. Each team had a decent balance of players who played 20-35 minutes per game and those who hovered around 10 minutes per game. Additionally, each distribution is quite wide with the average standard deviation among these teams being 10.86 minutes. The teams who finished the regular season in last place had an average standard deviation 7.74 minutes per game. In general, teams who finished the regular season in first place had a wider distribution of average minutes played per athlete, meaning that they were willing to play deeping into their rosters. This indicates that teams who ended up winning the league often had more depth than those towards the bottom of the rankings.  
  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; In 2020, the Las Vegas aces had a high density of players who played around 18-25 minutes per game with some players averaging 5-18 minutes per game. In 2021, the Connecticut Sun had a large cluster of players averaging around 30 minutes per game and they were supported by a smaller group of role players who played between 5 and 15 minutes per game. In 2022 the Aces had a large density of players who  averaged around ten minutes per game. They also had a smaller group of players who averaged about 30 minutes per game. The following year the Aces’ distribution saw similar values in which the peaks occurred at 10 and 30 minutes respectively. However, the density of those values changed. In 2023 the Aces had a larger group of players who averaged 30 minutes compared to the smaller support players who averaged 10 minutes per game. 2024 saw the New York Liberty have the most uniform playing time distribution of all of the first-place finishing teams. They too had players who appeared to average 30 minutes and players who averaged 10 minutes but the density of those groups was quite similar.   

### *Championship Winning Teams:*  

{% include_relative figures/Title.html %}

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; The playoff playing time distributions are much more similar than the other two groups already examined. All distributions are bimodal with dense clusters/peaks around 10 minutes and 30 minutes per game. There are no peaks at 20 minutes per game, an attribute often seen in team’s regular season distributions, or among teams that performed poorly in the playoffs. Therefore, teams who consistently play their star players upwards of thirty minutes, assisted by role players who play between ten and fifteen minutes per game have proven to be extremely successful in the postseason. 

# Conclusion

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; So, do successful teams only play their best players the majority of the game, or do they utilize their entire bench and evenly distribute the load? The results of these distributions indicate that it depends on how one defines success. In the regular season, it appears that teams who had wider distributions tended to end up higher in the rankings.  For example, the distributions of the number one ranked team during the regular season had an average standard deviation of 10.86 minutes per game compared to the twelfth ranked teams who had an average standard deviation of 7.74 minutes per game. Therefore, teams who play more players appear to perform better in the regular season than those who have limited depth.  
	
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; A potential drawback to this conclusion is that teams who end the regular season with a higher ranking may be winning games by insurmountable margins. When this occurs, say when a team is up by thirty points, they tend to play bench players who don’t always see the floor. That said, opposing teams often realize that the probability of them winning the game is low and too put their bench players in. This could be a contributing factor to the conclusion above but most likely is insufficient to fully dismiss it.   
	
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; However, playoff success has a different look to it. All of the recent WNBA champions had a bimodal playoff distribution with peaks at 10 and 30 minutes per game. This is an indication of consistency throughout all playoff games and the necessity of elite players complimented by utility players. There was no instance within the last five years where the WNBA championship winning team had a playoff distribution that was uniform or unimodal. A perfect case study is the Las Vegas Aces. Their championship earning years (2022 and 2023\) saw the team employ a bimodal distribution of playing time. Their stars played the majority of the game while the reserves aided their efforts through fewer but meaningful minutes. When the Aces failed to claim the title in 2020 and 2021 their distribution was unimodal and narrow indicating a more even distribution of playing time among stars and support players. Each of these years, the Aces entered the playoffs as either the 1 or 2 seed. While a bimodal distribution does not guarantee an eventual title win, it has been the strategy that the last five championship teams have harnessed.  

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; To further explore this topic, it would be beneficial to examine the average number of players that teams used throughout the regular season and playoffs. Additionally, rosters in the WNBA are subject to constant changes throughout the season due to trades, injury and suspension. While a few examples of these confounding factors were touched on, a deeper analysis of a team’s movements can tell a more comprehensive story about the success of a team. Additionally, examining how the distribution of playing time changes throughout the regular season, such as before and after the trade deadlines, would be fascinating. Not only could the distributions be drastically different before and after, but they may also average out the results above, potentially obscuring the true nuances of team dynamics. 

#### Works Cited

[^1]:  “WNBA.” *WNBA Stats*, stats.wnba.com/. Accessed 7 Dec. 2024\. 

[^2]:  “WNBA Standings \- 2024 Regular Season League Standings.” *ESPN*, ESPN Internet Ventures, www.espn.com/wnba/standings/\_/season/2024. Accessed 7 Dec. 2024\. 

[^3]:  Sun-Times, Chicago. “Chicago Sky Select Kamilla Cardoso and Angel Reese in 2024 WNBA Draft.” *Vocalo Radio 91.1FM*, Vocalo Radio 91.1FM, 17 Apr. 2024, vocalo.org/chicago-sky-sun-times-wnba-draft/. 

[^4]:  NBA. “3-Time WNBA Champion Candace Parker Announces Retirement.” *NBA.Com*, NBA.com, 28 Apr. 2024, www.nba.com/news/candace-parker-announces-retirement-wnba. 

[^5]:  Philippou, Alexa. “Napheesa Collier’s Comeback: From Giving Birth to Making Her WNBA Season Debut in 74 Days.” *ESPN*, ESPN Internet Ventures, www.espn.com/wnba/story/\_/id/34389238/napheesa-collier-comeback-giving-birth-making-wnba-season-debut-74-days. Accessed 7 Dec. 2024\. 

[^6]:  “Return to Play 2020.” *WNBA Stats*, 2020, stats.wnba.com/returntoplay2020/. 
