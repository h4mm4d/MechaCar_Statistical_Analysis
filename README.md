# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG

#################################################################
Call:
lm(formula = mpg ~ vehicle_length + vehicle_weight + spoiler_angle + 
    ground_clearance + AWD, data = mecha_mpg)

Residuals:
     Min       1Q   Median       3Q      Max 
-19.4701  -4.4994  -0.0692   5.4433  18.5849 

Coefficients:
                   Estimate Std. Error t value Pr(>|t|)
(Intercept)      -1.040e+02  1.585e+01  -6.559 5.08e-08
vehicle_length    6.267e+00  6.553e-01   9.563 2.60e-12
vehicle_weight    1.245e-03  6.890e-04   1.807   0.0776
spoiler_angle     6.877e-02  6.653e-02   1.034   0.3069
ground_clearance  3.546e+00  5.412e-01   6.551 5.21e-08
AWD              -3.411e+00  2.535e+00  -1.346   0.1852
                    
(Intercept)      ***
vehicle_length   ***
vehicle_weight   .  
spoiler_angle       
ground_clearance ***
AWD                 
---
Signif. codes:  
0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 8.774 on 44 degrees of freedom
Multiple R-squared:  0.7149,	Adjusted R-squared:  0.6825 
F-statistic: 22.07 on 5 and 44 DF,  p-value: 5.35e-11
######################################################################
R Summary Output for Predicted MPG for a sample of 50 cars 


In above summary vehicle length and ground clearance have p-value < 0.05 therefore rejects null hypothesis H0 and spoiler angle, and AWD options are not significant, therefore may not have significant affect on MPG and fails to reject null hypothesis. Vehicle weight is significant at 0.1 confidence interval. Since, mpg varies for many different reasons and confidence level should not be too strict I would recommend that to improve mpg along with ground clearance, and vehicle length, vehicle weight shoul dbe considered as well.  
This is definitly not a zero slope linear model. However, slope of AWd option and spoilet angle are close to zero. 
There is strong evidence that vehicle length and clearnace does affect mpg and somewhat weight as well. Therefore, based on these critara mpg of a prototype could be predited to certain degrees.   


## Summary Statistics on Suspension Coils

##############################################################################
#### total_summary
  Mean_PSI      Median_PSI  Var_PSI     Std_Dev_PSI     Num_Coil
1  1498.78       1500       62.29356    7.892627        150

#### lot_summary
  Manufacturing_Lot     Mean_PSI    Median_PSI  Var_PSI     Std_Dev_PSI      Num_Coil
1 Lot1                  1500        1500        0.980       0.990           50
2 Lot2                  1500.       1500        7.47        2.73            50
3 Lot3                  1496.       1498.       170.        13.0            50
##############################################################################