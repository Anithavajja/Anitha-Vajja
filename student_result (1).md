```python

```


```python

import pandas as pd

df2 = pd.DataFrame({
    "names": ['vineet', 'hisham', 'raj', 'ajeet', 'sujit', 'ramesh', 'priya', 'priyanka', 'suresh', 'ritesh', 'hitesh', 'jatin', 'chitesh', 'suman', 'raman', 'aman', 'ravi', 'shravi', 'chavvi', 'himanshu'],
    "rno": ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10', '11', '12', '13', '14', '15', '16', '17', '18', '19', '20']
})

print(df2)

```

           names rno
    0     vineet   1
    1     hisham   2
    2        raj   3
    3      ajeet   4
    4      sujit   5
    5     ramesh   6
    6      priya   7
    7   priyanka   8
    8     suresh   9
    9     ritesh  10
    10    hitesh  11
    11     jatin  12
    12   chitesh  13
    13     suman  14
    14     raman  15
    15      aman  16
    16      ravi  17
    17    shravi  18
    18    chavvi  19
    19  himanshu  20
    


```python
df3=pd.DataFrame({
    "results":['fail','fail','pass','pass','fail','pass','fail','pass','pass','pass','pass','fail','fail','fail','pass','fail','pass','fail','pass','pass'],
    "rno":['1','2','3','4','5','6','7','8','9','10','11','12','13','14','15','16','17','18','19','20']
    })
print(df3)
```

       results rno
    0     fail   1
    1     fail   2
    2     pass   3
    3     pass   4
    4     fail   5
    5     pass   6
    6     fail   7
    7     pass   8
    8     pass   9
    9     pass  10
    10    pass  11
    11    fail  12
    12    fail  13
    13    fail  14
    14    pass  15
    15    fail  16
    16    pass  17
    17    fail  18
    18    pass  19
    19    pass  20
    


```python
import pandas as pd
import numpy as np

```


```python
df=pd.merge(df2,df3)
df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>names</th>
      <th>rno</th>
      <th>results</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>vineet</td>
      <td>1</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>1</th>
      <td>hisham</td>
      <td>2</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>2</th>
      <td>raj</td>
      <td>3</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ajeet</td>
      <td>4</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>4</th>
      <td>sujit</td>
      <td>5</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>5</th>
      <td>ramesh</td>
      <td>6</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>6</th>
      <td>priya</td>
      <td>7</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>7</th>
      <td>priyanka</td>
      <td>8</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>8</th>
      <td>suresh</td>
      <td>9</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ritesh</td>
      <td>10</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>10</th>
      <td>hitesh</td>
      <td>11</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>11</th>
      <td>jatin</td>
      <td>12</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>12</th>
      <td>chitesh</td>
      <td>13</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>13</th>
      <td>suman</td>
      <td>14</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>14</th>
      <td>raman</td>
      <td>15</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>15</th>
      <td>aman</td>
      <td>16</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>16</th>
      <td>ravi</td>
      <td>17</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>17</th>
      <td>shravi</td>
      <td>18</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>18</th>
      <td>chavvi</td>
      <td>19</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>19</th>
      <td>himanshu</td>
      <td>20</td>
      <td>pass</td>
    </tr>
  </tbody>
</table>
</div>




```python
#students who cleared the exam
passed_students=df[df["results"]=="pass"]
passed_students
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>names</th>
      <th>rno</th>
      <th>results</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>2</th>
      <td>raj</td>
      <td>3</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>3</th>
      <td>ajeet</td>
      <td>4</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>5</th>
      <td>ramesh</td>
      <td>6</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>7</th>
      <td>priyanka</td>
      <td>8</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>8</th>
      <td>suresh</td>
      <td>9</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ritesh</td>
      <td>10</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>10</th>
      <td>hitesh</td>
      <td>11</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>14</th>
      <td>raman</td>
      <td>15</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>16</th>
      <td>ravi</td>
      <td>17</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>18</th>
      <td>chavvi</td>
      <td>19</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>19</th>
      <td>himanshu</td>
      <td>20</td>
      <td>pass</td>
    </tr>
  </tbody>
</table>
</div>




```python
#count number of students
count_results=df["results"].value_counts()
count_results
```




    pass    11
    fail     9
    Name: results, dtype: int64




```python
#arrange names by alpha based
alpha=df.sort_values(by='names')
alpha
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>names</th>
      <th>rno</th>
      <th>results</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>3</th>
      <td>ajeet</td>
      <td>4</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>15</th>
      <td>aman</td>
      <td>16</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>18</th>
      <td>chavvi</td>
      <td>19</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>12</th>
      <td>chitesh</td>
      <td>13</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>19</th>
      <td>himanshu</td>
      <td>20</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>1</th>
      <td>hisham</td>
      <td>2</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>10</th>
      <td>hitesh</td>
      <td>11</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>11</th>
      <td>jatin</td>
      <td>12</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>6</th>
      <td>priya</td>
      <td>7</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>7</th>
      <td>priyanka</td>
      <td>8</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>2</th>
      <td>raj</td>
      <td>3</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>14</th>
      <td>raman</td>
      <td>15</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>5</th>
      <td>ramesh</td>
      <td>6</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>16</th>
      <td>ravi</td>
      <td>17</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>9</th>
      <td>ritesh</td>
      <td>10</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>17</th>
      <td>shravi</td>
      <td>18</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>4</th>
      <td>sujit</td>
      <td>5</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>13</th>
      <td>suman</td>
      <td>14</td>
      <td>fail</td>
    </tr>
    <tr>
      <th>8</th>
      <td>suresh</td>
      <td>9</td>
      <td>pass</td>
    </tr>
    <tr>
      <th>0</th>
      <td>vineet</td>
      <td>1</td>
      <td>fail</td>
    </tr>
  </tbody>
</table>
</div>




```python

```


```python

```
