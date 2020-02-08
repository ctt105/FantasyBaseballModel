# fantasy-baseball-pipeline

Predictive model that orders MLB players by where they should be drafted and changes dynamically with each subsequent draft pick based on player value and team need. This is based on ESPN's ROTO league, with standard scoring rules.

### ESPN Rotisserie (ROTO)

  ROTO is one of the most common scoring formats for fantasy baseball. At the end of the season, points are totaled between categories specified before the season. For our pipeline, we kept traditional statistical categories: for batters, these include total bases (TB), home runs (HR), average (AVG), on base plus slugging (OPS), stolen bases (SB), walks (BB), and runs batted in (RBI). For pitchers, these include strikeouts (K), wins (W), saves (S), walks (BB), earned runs (ERA), and walks/hits per inning pitched (WHIP). Though we tried to keep categories that were most common among fantasy baseball leagues, the model could be used with any conceivable categories. 

  The rosters include: Rosters: one catcher (C), one first baseman (1B), one second baseman (2B), one shortstop (SS), one third baseman (3B), one middle infielder (MI) -- filled by a 2B/SS, one corner infielder (CI) -- filled by a 1B/3B, five outfielders (OF), one utility (UTIL) spot -- filled by any position, nine pitchers (P), and three bench (BE) spots -- those who are on your bench are players who are on your roster but not in your starting lineup.


### Data

  The dat we are using is from the Steamers projections for the 2020 season. Initially, we wanted to build our own projection system, but realized this would be more difficult due to playing time considerations than initially thought (for example, projecting a highly ranked prospect who only had 100 at bats, or a player who was injured for the majority of the season). So, we decided to use a pre-existing projection database, and to build our dynamic model using this.


### Draft Value

ESPN's draft system orders players based on the median assessment of value by several predetermined analysts (for example, if three analysts believe a player should be drafted 10, and one believes they should be drafted 12, they will have an average of 10.5). This will display for the person drafting, so they can default to experts if need be. However, this model does not evolve as a person continues to draft their team, and as players come off the board. This means that if the person has drafted no pitchers, but other teams have been specifically targeting pitchers, the model does not change its weighting of pitcher value from pre-draft rankings. Our model attempts to fix this, and integrate an updated weight based not only on projected player performance, but also on an individual team's needs. 
