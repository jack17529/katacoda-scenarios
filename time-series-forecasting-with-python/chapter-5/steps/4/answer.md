<pre class="file" data-target="clipboard">
# Hint: You can copy Solution to ClipBoard from Solution Tab
# create lag features
from pandas import read_csv
from pandas import DataFrame
from pandas import concat
series = read_csv('routine-heat.csv', header=0, index_col=0, parse_dates=True, squeeze=True)
temps = DataFrame(series.values)
dataframe = concat([temps.shift(3), temps.shift(2), temps.shift(1), temps], axis=1)
dataframe.columns = ['t-2', 't-1', 't', 't+1']
print(dataframe.head(7))
</pre>

