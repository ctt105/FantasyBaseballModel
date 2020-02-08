# fantasy-baseball-pipeline

Predictive model that orders MLB players by where they should be drafted. This is based on ESPN's ROTO league, with standard scoring rules.

### ESPN Rotisserie (ROTO)

  ROTO is one of the most common scoring formats for fantasy baseball. At the end of the season, points are totaled between categories specified before the season. For our pipeline, we kept traditional statistical categories: for batters, these include total bases (TB), home runs (HR), average (AVG), on base plus slugging (OPS), stolen bases (SB), walks (BB), and runs batted in (RBI). For pitchers, these include strikeouts (K), wins (W), saves (S), walks (BB), earned runs (ERA), and walks/hits per inning pitched (WHIP). Though we tried to keep categories that were most common among fantasy baseball leagues, the model could be used with any conceivable categories. 

  The rosters include: Rosters: one catcher (C), one first baseman (1B), one second baseman (2B), one shortstop (SS), one third baseman (3B), one middle infielder (MI) -- filled by a 2B/SS, one corner infielder (CI) -- filled by a 1B/3B, five outfielders (OF), one utility (UTIL) spot -- filled by any position, nine pitchers (P), and three bench (BE) spots -- those who are on your bench are players who are on your roster but not in your starting lineup.


### Data

  The data we used was downloaded from baseball savant's statcast customizable leaderboards. We then found which features correlated best with value added to a fantasy team. 
