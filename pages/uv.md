tags:: [[data-eng]], [[python]]

- # The pip interface
- ## Locking requirements.txt[^1]
	- ```bash
	  uv pip compile pyproject.toml -o requirements.txt
	  ```
- ## Upgrading requirements[^2]
	- ```bash
	  uv pip compile - -o requirements.txt --upgrade
	  ```
- # Running scripts[^3]
	- ```bash
	  uv run example.py
	  ```
- # References
	- [^1]: https://docs.astral.sh/uv/pip/compile/#locking-requirements
	- [^2]: https://docs.astral.sh/uv/pip/compile/#upgrading-requirements
	- [^3]: https://docs.astral.sh/uv/guides/scripts/#running-scripts