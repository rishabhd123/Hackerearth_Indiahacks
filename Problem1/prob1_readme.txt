Objective: 
To predict the orientation of a roadsign with respect to the front of a car, given it's angle, Aspect ratio & camera that detected it.

Quite a straight-forward problem, nothing fancy in terms of feature engineering.
I found a leak early on, which helped me gain a sizeable lead over most others. 
The ordering of rows was crucial, & targets could be inferred by analyzing neighbouring rows (i.e similar row_num percentile)
in the training set.

Models: weighted average of 1 XGB & 1 LightGBM. (Though single XGB scored almost the same)

Score: 0.0955 Logloss on CV, ~ 0.09 Logloss on Public LB (was good enough for 2nd place for this problem). 

