# SIMPLE-API
A package that will help on creating session upon making rest API request.

Sample usage:
```commandline
import logging

from src import RestApi


class TestApis:
    def __init__(self, base_url=""):
        self.client = RestApi(base_url=base_url)

    def get_upload(self):
        return self.client.get(path="/v3.1/name/indonesia")


if __name__ == '__main__':
    logging.basicConfig(level=logging.INFO, format="%(asctime)s - %(levelname)s - %(message)s")

    api = TestApis(base_url="https://restcountries.com")
    api.get_upload().status_code

```
