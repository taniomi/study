tags:: [[data-eng]] , [[python]]

- # Slicing correctly[^1]
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
- # Method Chaining with .pipe()[^2]
- # References
	- [^1]: https://www.kdnuggets.com/2020/04/stop-hurting-pandas.html
	- [^2]: https://tomaugspurger.net/posts/method-chaining/