# Stat_435_Homework_3

1) Beginning with the logistic regression model written as
π = exp(β0 + β1x1 + · · · + βpxp)
1 + exp(β0 + β1x1 + · · · + βpxp) ,
show that it leads to the model written as logit(π) = β0 + β1x1 + · · · + βpxp and vice
versa.

2) The failure of an O-ring on the space shuttle Challenger’s booster rockets led to its
destruction in 1986. Using data on previous space shuttle launches, Dalal et al. (1989)
examine the probability of an O-ring failure as a function of temperature at launch
and combustion pressure. Data from their paper is included in the challenger.csv file.
Below are the variables:
• Flight: Flight number
• Temp: Temperature (F) at launch
• Pressure: Combustion pressure (psi)
• O.ring: Number of primary field O-ring failures
• Number: Total number of primary field O-rings (six total, three each for the two
booster rockets)
The response variable is O.ring, and the explanatory variables are Temp and
Pressure. Complete the following:
(a) The authors use logistic regression to estimate the probability an O-ring will fail.
In order to use this model, the authors needed to assume that each O-ring is
independent for each launch. Discuss why this assumption is necessary and the
potential problems with it. Note that a subsequent analysis helped to alleviate
the authors’ concerns about independence.
(b) Estimate the logistic regression model using the explanatory variables in a linear
form.
(c) Perform LRTs to judge the importance of the explanatory variables in the model.
(d) The authors chose to remove Pressure from the model based on the LRTs. Based
on your results, discuss why you think this was done. Are there any potential
problems with removing this variable?

3) Continuing Exercise 4, consider the simplified model logit(π) = β0 + β1Temp, where π
is the probability of an O-ring failure. Complete the following:
(a) Estimate the model.
130 Analysis of Categorical Data with R
(b) Construct two plots: (1) π vs. Temp and (2) Expected number of failures vs. Temp.
Use a temperature range of 31◦ to 81◦ on the x-axis even though the minimum
temperature in the data set was 53◦.
(c) Include the 95% Wald confidence interval bands for π on the plot. Why are the
bands much wider for lower temperatures than for higher temperatures?
(d) The temperature was 31◦ at launch for the Challenger in 1986. Estimate the
probability of an O-ring failure using this temperature, and compute a corre-
sponding confidence interval. Discuss what assumptions need to be made in
order to apply the inference procedures.

4) Exercise 17 of Chapter 1 examined data from Berry and Wood (2004) to determine if
if an “icing the kicker” strategy implemented by the opposing team would reduce the
probability of success for a field goal. Additional data collected for this investigation
are included in the placekick.BW.csv file. Below are descriptions of the variables
available in this file:
• GameNum: Identifies the year and game
• Kicker: Last name of kicker
• Good: Response variable ("Y" = success, "N" = failure)
• Distance: Length in yards of the field goal
• Weather: Levels of "Clouds", "Inside", "SnowRain", and "Sun"
• Wind15: 1 if wind speed is ≥15 miles per hour and the placekick is outdoors, 0
otherwise.
• Temperature: Levels of "Nice" (40◦F < temperature < 80◦ or inside a dome),
"Cold" (temperature ≤ 40◦ and outdoors), and "Hot" (temperature ≥ 80◦ and
outdoors)
• Grass: 1 if kicking on a grass field, 0 otherwise
• Pressure: "Y" if attempt is in the last 3 minutes of a game and a successful field
goal causes a lead change, "N" otherwise
• Ice: 1 if Pressure = 1 and a time-out is called prior to the attempt, 0 otherwise
Notice that these variables are similar but not all are exactly the same as given for
the placekicking data described in Section 2.2.1 (e.g., information was collected on
field goals only, so there is no PAT variable). Using this new data set, complete the
following:
(a) When using a formula argument value of Good ~ Distance in glm(), how do
you know if R is modeling the probability of success or failure? Explain.
(b) Estimate the model from part (a), and plot it using the curve() function.
