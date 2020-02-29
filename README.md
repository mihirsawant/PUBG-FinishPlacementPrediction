# PUBG-FinishPlacementPrediction

## Dataset Link:
https://www.kaggle.com/c/pubg-finish-placement-prediction/data

## Abstract:
>In a PUBG game, up to 100 players start in each match (matchId). Players can be on teams (groupId) which get ranked at the end of the game (winPlacePerc) based on how many other teams are still alive when they are eliminated. In game, players can pick up different munitions, revive downed-but-not-out (knocked) teammates, drive vehicles, swim, run, shoot, and experience all of the consequences -- such as falling too far or running themselves over and eliminating themselves.
>We are provided with a large number of anonymized PUBG game stats, formatted so that each row contains one player's post- The data comes from matches of all types: solos, duos, squads, and custom; there is no guarantee of there being 100 players per match, nor at most 4 player per group.
>We will create a model which predicts players' finishing placement based on their final stats, on a scale from 1 (first place) to 0 (last place).<br><br><br>
##Data fields
>4. damageDealt - Total damage dealt. Note: Self inflicted damage is subtracted.<br>
>5. headshotKills - Number of enemy players killed with headshots.<br>
>6. heals - Number of healing items used.<br>
>8. Id - Player’s Id<br>
>9. killPlace - Ranking in match of number of enemy players killed.<br>
>10. killPoints - Kills-based external ranking of player. (Think of this as an Elo ranking where only kills matter.) If there is a value other than -1 in rankPoints, then any 0 in killPoints should be treated as a “None”.<br>
>11. killStreaks - Max number of enemy players killed in a short amount of time.<br>
>12. kills - Number of enemy players killed.<br>
>13. longestKill - Longest distance between player and player killed at time of death. This may be misleading, as downing a player and driving away may lead to a large longestKill stat.<br>
>14. matchDuration - Duration of match in seconds.<br>
>15. matchId - ID to identify match. There are no matches that are in both the training and testing set.<br>
>16. matchType - String identifying the game mode that the data comes from. The standard modes are “solo”, “duo”, “squad”, “solo-fpp”, “duo-fpp”, and “squad-fpp”; other modes are from events or custom matches.<br>
>17. rankPoints - Elo-like ranking of player. This ranking is inconsistent and is being deprecated in the API’s next version, so use with caution. Value of -1 takes place of “None”.<br>
>18. revives - Number of times this player revived teammates.<br>
>19. rideDistance - Total distance traveled in vehicles measured in meters.<br>
>20. roadKills - Number of kills while in a vehicle.<br>
>21. swimDistance - Total distance traveled by swimming measured in meters.<br>
>22. teamKills - Number of times this player killed a teammate.<br>
>23. vehicleDestroys - Number of vehicles destroyed.<br>
>24. walkDistance - Total distance traveled on foot measured in meters.<br>
>25. weaponsAcquired - Number of weapons picked up.<br>
>26. winPoints - Win-based external ranking of player. (Think of this as an Elo ranking where only winning matters.) If there is a value other than -1 in rankPoints, then any 0 in winPoints should be treated as a “None”.<br>
>27. groupId - ID to identify a group within a match. If the same group of players plays in different matches, they will have a different groupId each time.<br>
>28. numGroups - Number of groups we have data for in the match.<br>
>29. maxPlace - Worst placement we have data for in the match. This may not match with numGroups, as sometimes the data skips over placements.<br>
>30. winPlacePerc - The target of prediction. This is a percentile winning placement, where 1 corresponds to 1st place, and 0 corresponds to last place in the match. It is calculated off of maxPlace, not numGroups, so it is possible to have missing chunks in a match.<br>
​
>1. DBNOs - Number of enemy players knocked.<br>
>2. assists - Number of enemy players this player damaged that were killed by teammates.<br>
>3. boosts - Number of boost items used.<br>
>4. damageDealt - Total damage dealt. Note: Self inflicted damage is subtracted.<br>
>5. headshotKills - Number of enemy players killed with headshots.<br>
>6. heals - Number of healing items used.<br>
>8. Id - Player’s Id<br>
>9. killPlace - Ranking in match of number of enemy players killed.<br>
>10. killPoints - Kills-based external ranking of player. (Think of this as an Elo ranking where only kills matter.) If there is a value other than -1 in rankPoints, then any 0 in killPoints should be treated as a “None”.<br>
>11. killStreaks - Max number of enemy players killed in a short amount of time.<br>
>12. kills - Number of enemy players killed.<br>
>13. longestKill - Longest distance between player and player killed at time of death. This may be misleading, as downing a player and driving away may lead to a large longestKill stat.<br>
>14. matchDuration - Duration of match in seconds.<br>
>15. matchId - ID to identify match. There are no matches that are in both the training and testing set.<br>
>16. matchType - String identifying the game mode that the data comes from. The standard modes are “solo”, “duo”, “squad”, “solo-fpp”, “duo-fpp”, and “squad-fpp”; other modes are from events or custom matches.<br>
>17. rankPoints - Elo-like ranking of player. This ranking is inconsistent and is being deprecated in the API’s next version, so use with caution. Value of -1 takes place of “None”.<br>
>18. revives - Number of times this player revived teammates.<br>
>19. rideDistance - Total distance traveled in vehicles measured in meters.<br>
>20. roadKills - Number of kills while in a vehicle.<br>
>21. swimDistance - Total distance traveled by swimming measured in meters.<br>
>22. teamKills - Number of times this player killed a teammate.<br>
>23. vehicleDestroys - Number of vehicles destroyed.<br>
>24. walkDistance - Total distance traveled on foot measured in meters.<br>
>25. weaponsAcquired - Number of weapons picked up.<br>
>26. winPoints - Win-based external ranking of player. (Think of this as an Elo ranking where only winning matters.) If there is a value other than -1 in rankPoints, then any 0 in winPoints should be treated as a “None”.<br>
>27. groupId - ID to identify a group within a match. If the same group of players plays in different matches, they will have a different groupId each time.<br>
>28. numGroups - Number of groups we have data for in the match.<br>
>29. maxPlace - Worst placement we have data for in the match. This may not match with numGroups, as sometimes the data skips over placements.<br>
>30. winPlacePerc - The target of prediction. This is a percentile winning placement, where 1 corresponds to 1st place, and 0 corresponds to last place in the match. It is calculated off of maxPlace, not numGroups, so it is possible to have missing chunks in a match.<br>
