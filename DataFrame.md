DataFrame is one of the simplest Data Structure is introduced in the python pandas.

DataFrames basically used to handle n no of rows and columns.

Each row and column is a numpy.Series object.

```
>>> import pandas as pd
>>> pd.DataFrame([])    # Create Empty DataFrame
```
Above command will create empty DataFrame.
```
>>> df = pd.DataFrame([[ _ for _ in range(1, 10)]])
```
Above command will create the dataFrame which have 9 columns and one row.
After the execution of the command it will look like :
```
   0  1  2  3  4  5  6  7  8
0  1  2  3  4  5  6  7  8  9
```
In above example 9 columns are created (0 to 8) and 1 - 9 is our data.
0 before 1 will denote the row no.

Now try to assign some column values on the data frame.
```
>>> df = pd.DataFrame([[ _ for _ in range(1, 10)]], columns=['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I'])
    A  B  C  D  E  F  G  H  I
0  1  2  3  4  5  6  7  8  9

```
Now we assigned names to each columns, Or you can do it using simple way like below:
```
>>> pd.DataFrame([[ _ for _ in range(1, 10)]], columns=list('ABCDEFGHI'))
   A  B  C  D  E  F  G  H  I
0  1  2  3  4  5  6  7  8  9
```
*Remember* While working with pandas, you need to pass equal no of columns as data content has.
