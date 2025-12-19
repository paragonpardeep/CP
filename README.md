fetch dt.entity.host
| filter entity.name in [
  "host01.example.com",
  "host02.example.com",
  "host03.example.com",
  "host04.example.com"
]
| fields entity.id, entity.name

