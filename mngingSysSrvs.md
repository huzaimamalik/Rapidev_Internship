Managing System Services:
systemctl enable/disable [service]
systemctl status [service]
systemctl restart/reload [service] -> reload makes the service re-read its config files while restart completely shuts down restarts the service
systemctl mask/unmask [service] -> mask stops the service from being started manually/automatic
