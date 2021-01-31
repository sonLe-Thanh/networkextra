# Multi-layer client-server network system

Currently works for 2-layer client-server interaction.

## WIP:
* Failsafe mechanism (i.e. unexpected crash of server(s))
* Sensible averaging algorithm
* Capability to send large files over socket

## Demo:
To run the 2-layer network simulation to calculate average number sent by clients, run the following command
```
python server.py
```
```
python internal_server.py
```
```
python client.py
```
You can run as many clients as possible for testing purpose.
## Changelog:
**Update client, edge**
* change client_conns of internal_server to dictionary type
* update the value and remove the old value of the client being connected
* client_ip variable now includes the port with format: ip_add:port
* add __del__ to client

**Update server, edge**
* change the data type that send from internal to server
* change the way that server and edge calculate the sum and average value
* knowned issue: the server and the edge should not run in the IDE terminal in order to shutdown them normally

**Solve critical section problem**
* solved issue: when deletes an client, the sum value of the server cannot change immediately
## Authors:
Current author: 
- [Le Thanh Son](https://github.com/sonLe-Thanh)
- [Nguyen Huu Thien Phu](https://github.com/phupfoem)
- [Hoang Tan Phat](https://github.com/hoangphatmonter)