# Mock FTP Server
**Objective** Build a mock FTP server that records port scan attempts and login activities through port 21. The mock FTP server should do the following:
1. Keep logs of login attempts of the *username, password, timestamps, source IP* and *TTL value* of the connection request.
2. Allow total of *THREE* login attempts; for each failed attempt, the program returns an error message to the client. After three attemps, the program terminate.
3. Record port scan activity (connection establishment without any login attempts)
4. Check up mechanism to periodially check for any activities over the measurement period to detect issues

This server will be up and running on a host machine for a total of at least 72 hours over at least three different time periods of 18 hours minimum. 

Make sure the host machine is "observable" to the internet, this can you done by configuring port 21 to be forwarded to the monitoring hosts which runs the server in your network.

While the server runs, also run Wireshark simultaneously during the experimentation time period so there will be two logs at the end of the measurement period. 