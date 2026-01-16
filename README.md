index=k8s_logs
kubernetes_container_name="fad-forward-sync-consumer"
| stats count by kubernetes_pod_name
