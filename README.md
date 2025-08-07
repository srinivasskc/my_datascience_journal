
## My Data Science and AI Learning Joural

Date 4/8/2025 - 6/8/2025: Completed the Python Crash Course.

#### Highlights:
- Used Jupyter Notebook on VSCode.
- Learnt New about Lambda Functions, Ternary Operator, List Comprehension.

## Installing Pandas
```
pip install pandas

Installing collected packages: pytz, tzdata, numpy, pandas

pd.__version__

To Check the pandas library version installed.
```


####  Statistics - Series in Pandas
```
References: 
Standard Deviation = https://www.youtube.com/watch?v=IaTFpp-uzp0
```

```
my_series_int.describe()
```

#### If my_series_int = pd.Series([10, 20, 30]):

count: No.of non-null elements in series 

    = n = 3

mean: = Average Value

    = Sum of numbers/size of sample = ((10 + 20 + 30) / 3 = 20 )

std: = Standard Deviation 

     = sqrt{(Sum(x-mean)^2)/(n-1)}
     = sqrt{((10-20)^2 + (20-20)^2 + (30-20)^2)/3-1}
     = sqrt{((-10)^2 + (0)^2 + (10)^2)/2}
     = sqrt{(100+0+100)/2}
     = sqrt{200/2}
     = sqrt{100}
     = 10
    
min: = Minimum value 
     
     = min = 10


### Formula Pandas Uses for Percentiles (like 25%)
For a sorted dataset with n values, the position of the percentile is calculated as:

Position = (n - 1) × P

n = number of data points

P = desired percentile (25% → 0.25, 50% → 0.50, etc.)

25% (First Quartile, Q1): This is the value below which 25% of the data falls.

For a sorted list: 
    
    = For [10, 20, 30], 25% is halfway between 10 and 20: ((10+20)/2=15)


50% (Median, Q2): The middle value. 

    =  For [10, 20, 30], it's 20.

75% (Third Quartile, Q3): The value below which 75% of the data falls.
    
    = For [10, 20, 30], it's halfway between 20 and 30: ((20+30)/2=25)


If the position is not an integer (e.g. 1.75), Pandas interpolates between the two nearest values.

Example: (7 - 1) × 0.25 = 6 × 0.25 = 1.5 (d=0.5)

Interpolated value=value_low+(value_high−value_low)×d

25% (First Quartile, Q1): =20+(30−20)×0.5= 20+(10×0.5) = 25.0 -- So Q1 = 25.0
etc.



max = Maximum Value
    
    = max = 30

## Lesson Learnt:

Statistics - Math Textbooks:
```
Q2 (Median): Always the middle value (or average of two middle values).
Q1 (25%) and Q3 (75%):
For odd-sized datasets, some textbooks take the median of the lower and upper halves (excluding or including the median itself).
Others use interpolation formulas.
```

In Pandas and NumPy:
```
Pandas uses linear interpolation (the "inclusive" method, also called method='linear' or method='inclusive' in NumPy 1.22+).
The position for the 25th percentile is calculated as:
[{Position} = (n - 1) x 0.25 ]
If the position is an integer, Pandas picks that value.
If not, it interpolates between the two closest values.

If you want to match a specific textbook method, you can use NumPy's percentile with different method arguments.
```