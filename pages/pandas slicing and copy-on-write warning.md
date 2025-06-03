tags:: [[pandas]]

- https://www.kdnuggets.com/2020/04/stop-hurting-pandas.html
- https://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#returning-a-view-versus-a-copy
- # Slicing correctly
	- Chained indexing effect occurs because pandas creates a copy when indexing like:
		- ```python
		  df[df['x'] == y]
		  ```
	- And it creates a view when indexing by selecting columns:
		- ```python
		  df['x']
		  ```
	- So if I want to change a value in column x, if I did as below, I would change the values to z on a copy.
		- ```python
		  df[df['x'] == y]['x'] = z
		  ```
- ## What to do
	- ```python
	  # if filtering on condition
	  df.loc[condition, 'column_name'] = new_value
	  
	  # if changing the entire column type, it is fine to do this
	  df['column_name'] = df['column_name'].astype(str)
	  
	  # e.g.
	  df.loc[df['x'] > y, 'x'] = z
	  df['x'] = df['x'].astype(str)
	  ```