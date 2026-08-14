# Torbin

# Description
Torbin is a simple tool for rotating your Tor circuit at specific time intervals. It automatically checks whether the Tor service is running; if not, it launches the service in the background. You can configure the interval in seconds and toggle *verbose* mode on or off.

We created this tool for prototyping purposes. In the future, we may switch to a more suitable language like C and adopt a more modular tool structure.

Currently, it only runs on Debian-based Linux distributions.

## Installation
This automatically install torbin and set tor service to run in background.

`curl -sL "https://raw.githubusercontent.com/synnaulaid/torbin/refs/heads/master/settor" | sudo bash`


## Usage
This is a simple tool to change your tor circuit in a specific interval. You can set the interval in seconds and also set verbose mode to true or false.

```
./torbin -h
-h                      Show all help command
-i <num of sec>         Set interval to change new circuit in sec <default 60>
-v <true/false>         Show verbose set true or silent verbose set false

example: ./torbin -i 10 -v true
[*] Starting Torbin 10 sec interval to change...
[*] Checking tor service ...
[*] Service up
-----------------------------------
[+] Torbin change to: 128.98.08.133
[+] Torbin change to: 28.98.28.143
[+] Torbin change to: 228.38.89.33
....
```
## Switch ON/OFF Tor Service
You can switch on/off tor service by using the following command.
`sudo ./tor-on or ./tor-off`