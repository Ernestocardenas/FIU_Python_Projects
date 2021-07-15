# Building Router 

Your router will receive raw Ethernet frames and process them just like a real router: forward them to the correct outgoing interface, 
create new frames, etc.

f your router is functioning correctly, all of the following operations should work:

ping from the client to any of the router’s interfaces:

  mininet> client ping 192.168.2.1
  ...
  mininet> client ping 172.64.3.1
  ...
  mininet> client ping 10.0.1.1
  ...
ping from the client to any of the app servers:

  mininet> client ping server1  # or client ping 192.168.2.2
  ...
  mininet> client ping server2  # or client ping 172.64.3.10
  ...
traceroute from the client to any of the router’s interfaces:

  mininet> client traceroute 192.168.2.1
  ...
  mininet> client traceroute 172.64.3.1
  ...
  mininet> client traceroute 10.0.1.1
  ...
Tracerouting from the client to any of the app servers:

  mininet> client traceroute server1
  ...
  mininet> client traceroute server2
  ...
Transferring file from client to server(s) using the code from your project 1 or 2. 
Notice that outputs need to be redirected into files; otherwise, the client or server(s) may stop responding.

  mininet> server1 /path/to/your/server.py 5000 /folder/to/save > server1Output &
  ...
  mininet> client /path/to/your/client.py 192.168.2.2 5000 /file/to/transfer > clientOutput &
  ...
