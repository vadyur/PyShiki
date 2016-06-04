# PyShiki
Python lib for working with [shikimori.org](http://shikimori.org/) api

Installing:
```
# Linux:
sudo pip3 install pyshiki

# Windows:
pip3 install pyshiki
```

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
dev = api.devices(device={"user_id": 23456813,
                          "token": "test",
                          "platform": "ios",
                          "name": "test"}).post()
pprint(dev)
```

## Changelog
#### v 1.1.3
+ Refactored code
+ Changed license to MIT
