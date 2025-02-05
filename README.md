# Used-Vehicles
The dataset contains various factors that may influence car prices , including :
Region : The geographical area where the car is listed.
Price : The listed price of the vehicle
Year : The manufacturing year of the vehicle 
Manufacturer & Model : The brand and specific model of the car
Condition : The general state of the vehicle - excellent , good, fair
Fuel Type : Gasoline , diesel , electric
Transmission : Manual or automatic
Size : Vehicle size category
Type : Car type - sedan , truck , SUV
Odometer : The number of miles driven is a key factor in pricing


I will first analyze missing data and then perform an exploratory analysis pf price determinants.

The dataset contains significant missing data, particularly in key variables like year , manufacturer , model , condition , fuel type, transmission and drive type .
Here are the key observations :
1 . Year : 1205 missing values. This is relatively small and could be handled by imputation.
2 . Manufacturer and Model : Manufacturer has 17646 missing values while model has 5277 missing .
3 . Condition , Drive : These have high percentage of missing values .
4 . Size & Type : Size is missing over 90% of cases making it unreliable for analysis.

I will begin by filtering out unrealistic prices (<=$100 or>$100000) , we have 389836 valid records. Here are some key statistics on car prices :
Mean Price : $18885
Median Price : $15,500
Price Range : $101 to $100000
IQR : 25th percentile - $7495 , 75th percentile - $27825

Correlation Analysis :
1. Year vs Price :
   Positive correlation , meaning newer cars tend to have hiher prices.
   The correlation is moderate , suggesting other factors also play a role.
2. Odometer vs Price :
   Negative Correlation meaning higher mileage tends to reduce the price.
   The correlation is weaker than year vs price but still significant.
3. Year vs odometer :
   Slight negative correlation meaning newer card tend to have lower mileage.

Insights from Scatter Plots :
1. Car Price vs Year:
   As expected , newer cars tend to have higher prices.
   There's a clear upward trend, particularly for cars made after 2010 , where prices remain higher.
   Older cars(before 2000) tend to be much cheaper.

2. Car Price vs Odometer:
    Cars with lower mileage tend to have higher prices.
   However , there's considerable variation meaning other factors - such as brand , condition , features influence pricing beyond just mileage.


I'll now analyze how different manufacturers affect car pricing asbrand reputation is a majore factor :
Luxury brands (Ferrari, Aston Martin , Tesla, Porsche , BMW , Audi) tend to have higher median prices
Economy brands (Honda, Toyota , Ford , Chevrolet, Nissan) show a much wider price range indicating a mix of budget and premium models.
The average and median prices reveal the typical cost of a car from each brand.
Standard deviation indicates price variation - higher values mean a mix of budget and high end models.
The count column shows the number of listings per manufacturer helping identify which brands are more common in dataset.
