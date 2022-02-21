# MechaCar_Statistical_Analysis

## Linear Regression to Predict MPG

![](https://github.com/h4mm4d/MechaCar_Statistical_Analysis/blob/main/fig3.PNG?raw=true)
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

Lot 1 and Lot 2 with variance on 1 and 7.5 ar emeeting the standard and lot 3 with variance of 170 ponds per square inch does not meet the standard. Therefore lot3 should be rejected. 

## T-Tests on Suspension Coils

#############################################################################
> t.test(mecha_coil$PSI,mu=1500)

	One Sample t-test

data:  mecha_coil$PSI
t = -1.8931, df = 149, p-value = 0.06028
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1497.507 1500.053
sample estimates:
mean of x 
  1498.78 

> lot1 <- subset(mecha_coil, Manufacturing_Lot=="Lot1")
> t.test(lot1$PSI,mu=1500)

	One Sample t-test

data:  lot1$PSI
t = 0, df = 49, p-value = 1
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.719 1500.281
sample estimates:
mean of x 
     1500 

> lot2 <- subset(mecha_coil, Manufacturing_Lot=="Lot2")
> t.test(lot2$PSI,mu=1500)

	One Sample t-test

data:  lot2$PSI
t = 0.51745, df = 49, p-value = 0.6072
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1499.423 1500.977
sample estimates:
mean of x 
   1500.2 

> lot3 <- subset(mecha_coil, Manufacturing_Lot=="Lot3")
> t.test(lot3$PSI,mu=1500)

	One Sample t-test

data:  lot3$PSI
t = -2.0916, df = 49, p-value = 0.04168
alternative hypothesis: true mean is not equal to 1500
95 percent confidence interval:
 1492.431 1499.849
sample estimates:
mean of x 
  1496.14 
#############################################################################

Over all Mecha_coil and lot 3 are significant enough to reject null hypothesis (H0). Therefore, there is significant issue with lot 3 that is causing whole data to be skewed. Lot 1 and lot 2 fails to reject null hypothesis on its own. Therefore, the variance in quality is statistically insignificant. 





