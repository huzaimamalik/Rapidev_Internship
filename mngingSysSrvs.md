Managing System Services:
systemctl enable/disable [service] -> enabling/disabling the service on startup
systemctl status [service] -> getting the status of the service
systemctl restart/reload [service] -> reload makes the service re-read its config files while restart completely shuts down restarts the service
systemctl mask/unmask [service] -> mask stops the service from being started manually/automatic
