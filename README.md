# PyShiki
Python lib for working with [shikimori.org])(http://shikimori.org/) api

****

## Examples
```python
import pyshiki
from pprint import pprint

api = pyshiki.Api("YOUR_NICKNAME", "YOUR_PASSWORD")

# GET  http://shikimori.org/api/animes/search?q=Lucky+Star
ls = api.animes("search", q="Lucky Star").get()
pprint(ls)

# POST http://shikimori.org/api/devices
# {
#   "device": {
#     "user_id": 23456813,
#     "token": "test",
#     "platform": "ios",
#     "name": "test"
#   }
# }
api.animes("devices" device={"user_id": 23456813,
                             "token": "test",
                             "platform": "ios",
                             "name": "test"}).post()

```