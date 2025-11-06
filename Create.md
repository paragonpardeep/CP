fetch metrics
| filter metric == "builtin:host.uptime"
| filter dt.entity.host == "HOST-XXXX"
