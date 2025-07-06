# Brute-Force-Attack-Detection
Splunk Use-case Brute Force Attack Detection
sourcetype="linux_secure" OR sourcetype="WinEventLog:Security" | search "failed" OR "authentication failure" | stats count by src_ip, user | where count > 10
