fetch dt.entity.host
| filter entity.name == "host01.example.com"
| fields entity.id, entity.name
