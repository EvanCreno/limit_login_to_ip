# Limit login to IP ranges

This app modifies modifies the login logic to only allow login from specified login
ranges.

The allowed IP addresses have to be passed via `occ app:config` as a string 
separated by comma.

For example to whitelist `127.0.0.0/24`: 

- `occ config:app:set limit_login_to_ip blocked.ranges --value 127.0.0.0/24`

To whitelist `127.0.0.0/24` and also `192.168.0.0/24`: 

- `occ config:app:set limit_login_to_ip blocked.ranges --value 127.0.0.0/24,192.168.0.0/24`