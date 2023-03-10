# HAproxy

HAProxy is a free, very fast and reliable reverse-proxy offering high availability, load balancing, and proxying for TCP and HTTP-based applications.

## Installation

Use the package manager [yum](https://pip.pypa.io/en/stable/) to install HAproxy.

```bash
yum install haproxy
```

## Config file

```python
path '/etc/haproxy/haproxy.cfg'

# stick tables 
watch -n 1 ' echo "show table " | socat /var/run/haproxy.sock'
watch -n 1 ' echo "show table " | nc -U /var/run/haproxy.sock'

# Logs
tail -f '/var/log/haproxy.log' 

#Lua 
#Lua is a lightweight programming language used to expand HAproxy Functionality
lua-load $PATH
```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.
