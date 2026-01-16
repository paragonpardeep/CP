index=* "fad-forward-sync-consumer" 325989
| stats count by index

index=* "fad-forward-sync-consumer" 325989
| stats count by sourcetype

index=* "fad-forward-sync-consumer" 325989
| table _time _raw

index=* "fad-forward-sync-consumer" 325989
| table _time _indextime

index=k8s_logs "fad-forward-sync-consumer" 325989
