tags:: [[python]]

- # Basic logging template
	- ```python
	  import logging
	  # Set up logging
	  logging.basicConfig(
	      level=logging.INFO,
	      format='%(asctime)s [%(levelname)s] %(message)s',
	      filename='./logs/logger.log',
	      datefmt='%Y-%m-%d %H:%M:%S'
	  )
	  ```