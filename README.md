
## My Data Science and AI Learning Joural

Date 4/8/2025 - 6/8/2025: Completed the Python Crash Course.

#### Highlights:
- Used Jupyter Notebook on VSCode.
- Learnt New about Lambda Functions, Ternary Operator, List Comprehension.

## Installing Pandas
```
pip install pandas

Installing collected packages: pytz, tzdata, numpy, pandas
```


####  Statistics - Series in Pandas
```
References: 
Standard Deviation = https://www.youtube.com/watch?v=IaTFpp-uzp0
Q1, Q2, Q3 = https://youtube.com/shorts/NySKuyBS3LM?si=G4osm_JTiZ-vqlbj
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

25% (First Quartile, Q1): This is the value below which 25% of the data falls.

For a sorted list: 
    
    = For [10, 20, 30], 25% is halfway between 10 and 20: ((10+20)/2=15)

50% (Median, Q2): The middle value. 

    =  For [10, 20, 30], it's 20.

75% (Third Quartile, Q3): The value below which 75% of the data falls.
    
    = For [10, 20, 30], it's halfway between 20 and 30: ((20+30)/2=25)

max = Maximum Value
    
    = max = 30

