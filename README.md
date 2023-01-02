<h1> monthly-expenses-analysis </h1>

Writing Python script to analyze export of monthly expenses from Mint.com and teach myself data analysis in Python.

Going off of Rob Mulla's videos on Youtube as a guide.

<i> EDA </i>

Started by installing Jupyterlab and importing pandas, numpy, matplotlib.pylab and seaborn
and then spreadsheet with pd.read_csv. Did initialy analysis with .shape, .head(), .columns,
.dtypes, and .describe()

<i> Data Prep </i>

Created subset specifying column names to keep in double brackets. Could also use .drop() to specify columns to remove.
With Python you have to use .copy() at the end to make sure it understands sub is separate variable.

Set Date column to date type with pd.to_datetime(). Can use pd.to_numeric() also. 
Renamed columns with .rename(columns={'oldname':'newname'})
checked for NAs with .isna().sum() to show totals per column
can also check for duplicates with .duplicated() and can use .loc[df.duplicated()] to find them
can also search more specifically with .query('column' == 'rowname')
Can use ~ to do inverse of function, such as ~df.duplicated() to show non-duplicates

If rows are removed, should use .reset_index(drop=True) to reset index but hide index column

<i> Feature Understanding </i>

Can use .value_counts() on column to order how many rows each value has.
Backslashes allow you to break up code
ax.set_xlabel() - set label for plot, good idea to define plots as separate from df
examples of plots: bar, hist, and kde

<i> Feature Relationships </i>

scatter another plot. Should use plt.show() at the end to remove the object description.
.dropna() to get rid of NA values
.corr() to show correlation

<i> What questions do I want to answer? </i>

Spending by week compare
Which day of week do we spend most
categories most spent
spending by person

.groupby and .agg other ways to subset

