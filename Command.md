**Encountered an error when testing a remote service.**

**Error:** WARNING: TCP connect to (XX.XXX.XXX.XXX : YYY) failed

**Troubleshooting:**
Follow the below order. These instructions are for Linux remote machine.
1. Check if you are able to ping server . Command : ping < servername >
2. Check if the port is opened on the server. Command : netstat -tulpn | grep LISTEN
3. If disabled, then you would need to run following commands based on the type,
   
     a.  Enable Port : firewall-cmd --permanent --zone=public --add-port=<Port>/tcp
   
     b.  Enable Service : firewall-cmd --permanent --zone=public --add-service=http

   
