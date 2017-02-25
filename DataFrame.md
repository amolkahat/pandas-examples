__DataFrame__ is one of the simplest Data Structure is introduced in the python pandas.

DataFrames basically used to handle n no of rows and columns.

Each row and column is a numpy.Series object.

#### Let's see how we can create DataFrame.
__pandas.DataFrame__ class will allow you to create data frame as you want.
```
>>> import pandas as pd
>>> pd.DataFrame()    # Create Empty DataFrame
```
We just created an empty DataFrame with no data, index.

Now let's create DataFrame with some data.
```
>>> df = pd.DataFrame([[ _ for _ in range(1, 10)]])
```
In above example we are creating the list which gives the numbers of 1 to 9.
After the execution of the command it will look like :
```
   0  1  2  3  4  5  6  7  8
0  1  2  3  4  5  6  7  8  9
```
Here (0 to 8) are the column lables which is by defalut assigned by DataFrame, and 1 - 9 is our data.
0 before 1 will denote the row no, or it is an index of the data.

##### Create DataFrame with labeled columns.
Using *columns* paramter in DataFrame we can lebel the columns.
```
>>> df = pd.DataFrame([[ _ for _ in range(1, 10)]], columns=['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I'])
    A  B  C  D  E  F  G  H  I
0  1  2  3  4  5  6  7  8  9

```
If you want you an use columns parameter like this :
```
>>> pd.DataFrame([[ _ for _ in range(1, 10)]], columns=list('ABCDEFGHI'))
   A  B  C  D  E  F  G  H  I
0  1  2  3  4  5  6  7  8  9
```
*Remember* While working with pandas, you need to pass equal no of columns as data content has.

Dataframe have following parameters : data, index, column, dtype and copy. We just saw the example of the columns. Now let's try with the index.

##### Create DataFrame with labeled index.
In above example i assigned A-I column labels to the DataFrame. Now let's try to assign same to the *index* parameter
```
>>> pd.DataFrame([[_ for _ in range(10)]], index=list('ABCDEFGHIJ')) 
   0  1  2  3  4  5  6  7  8  9
A  0  1  2  3  4  5  6  7  8  9
B  0  1  2  3  4  5  6  7  8  9
C  0  1  2  3  4  5  6  7  8  9
D  0  1  2  3  4  5  6  7  8  9
E  0  1  2  3  4  5  6  7  8  9
F  0  1  2  3  4  5  6  7  8  9
G  0  1  2  3  4  5  6  7  8  9
H  0  1  2  3  4  5  6  7  8  9
I  0  1  2  3  4  5  6  7  8  9
J  0  1  2  3  4  5  6  7  8  9
```
In above example we assign list('ABCDEFGHI') to the index field. Remember we provide only row 'A' data. By default pandas copy the first row data to another row and completed the DataFrame.

Let's do some other experiments with DataFrame. Now try to pass dict to the index prameter in the DataFrame.
```
>>> pd.DataFrame([[_ for _ in range(10)]], index={'A': 1, 'B':2})
   0  1  2  3  4  5  6  7  8  9
A  0  1  2  3  4  5  6  7  8  9
B  0  1  2  3  4  5  6  7  8  9
```

it works for dict too. When dict is passed to the DataFrame it will take it's keys as an index. For practice you can try it with the tuples.

