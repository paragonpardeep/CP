fetch dt.host
| fields hostname, uptime
| filter hostname == "your-hostname"
