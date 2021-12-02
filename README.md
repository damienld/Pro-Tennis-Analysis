# TennisData
 Data analysis from professional tennis matches

## Aces_Regression

The goal here is to **to predict the actual Ace rate (how many aces he hit by point) of a player for one match** from: 
- AvgAceRateP: the **average ace rate of the player** (on clay or non clay surface) over past seasons. It is calculated from all the matches on this specficic surface over the past 3 seasons and weighted by date of season.
- AvgAceRateOpp: the **average conceded ace rate of the opponent** (on clay or non clay surface) over past seasons. It is calculated from all the matches on this specficic surface over the past 3 seasons and weighted by date of season.
- TrnSpeed: the **speed of the tournament** (standard speed is 1.0)

We will use the **actual ace rate** of a match to train the model.

This notebook uses some personal data on ATP tennis matches since 2016. The data includes a lot of common statistics about each match:
- result
- score
- points won on serve
- CourtId: 1 to 6: "Hard", "Clay", "Indoor", "Carpet", "Grass", "Acrylic"
- aces...

Each match is made of 2 rows:
- the first row contains the stats for the first player
- the second row for the second player


## WHR0

This notebooks **tests the WHR rating meta model** developped by Remy Coulom. It is a strong alternative to ELO or Glicko traditional models used to rate players in Chess. https://hal.inria.fr/inria-00323349/document/

WHR0 is the python implementation from here: https://github.com/pfmonville/whole_history_rating

It applies the WHR rating model to ATP tennis matches to see if it can fit.
