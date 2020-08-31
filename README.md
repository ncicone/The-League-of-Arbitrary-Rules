# About the code
This code is a Python script utilizing jquery and Selenium. It was written to support the faciliation of a FantasyPremierLeague Classic League that I hosted for the 2020/2021 season. Most of this code will prove useful for those managing classic leagues requiring elimination.  
Note that I have not yet coded everything.  
Currently coded:  
  1. a way to scrape the FPL website to get all the league managers' team names, team ids, and manager first and last name (See "Scraping FPL for league information")  
  2. a way to automate the removal of players from the league once eliminated (See "Automating eliminated players from league")   
Need to code:  
  3. collecting manager GW score and total score, automatically calculating the number of eliminated managers and the elimination thresholds.. may just do in Excel each week so        don't count on this being uploaded  


The following is info on the League I hosted
# The League of Arbitrary Rules
This is the code file for The League of Arbitrary Rules- a Fantasy Premier League run on fantasy.premierleague.com.
Rules for the league:
  1. players who finish the GW with a round number (0,10,20,...,100) will be eliminated
  2. players failing to score 10 points in any GW will be eliminated
  3. players ending any GW with a total score equal to a multiple of 1,000 will be eliminated
  4. hits may or may not count: whatever data included at https://fantasy.premierleague.com/api/entry/TEAMID/event/GAMEWEEK/picks/ where TEAMID and GAMEWEEK are the participating        FPL manager's unique team ID and gameweek for which points have accumulated. If the GW total includes hits, then hits are included. (Still need to code once league kicks          off)
  5. there's a safety threshold (12%) : if the number of players that shall get eliminated is more than 12% of the number of remaining players, everybody is safe and nobody gets          eliminated. The number of players getting eliminated calculation includes any of the 3 elimination methods discussed above in Rules 1, 2, & 3.
  6. the elimination phase stops at GW34 : if you are lucky enough to be on the league after that, you are safe for the rest of the season
  7. the winner : the winner is, among those remaining in the league, the player with the most overall points
  8. as an exception, if my own team finishes with a round number, I will not eliminate it so I can continue to administer the league. However, my team would be eliminated and no         longer included in any calculations going forward
  9. no new teams will be admitted to the league after GW1
  10. one team per manager
