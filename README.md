# Performance Analysis on Fabric Testbed : 

# Fabric testbed iperf experiment example

Experiment 1 : Available ethernet traffic throughput on Fabric testbed inside switch : 

```
15.6 Gbits/sec
```

![Screenshot from 2023-06-16 12-17-48](https://github.com/nagmat1/fabric_ethernet_througput_exp/assets/51871069/f20082fc-2aa4-44f8-8978-1648be36c264)

# Experiment 2 : 

What is the maximum throughput with ``` sendpfast ``` : It is ``` 11962.36 KB/s ```

![Screenshot from 2023-06-16 19-02-37](https://github.com/nagmat1/fabric_ethernet_througput_exp/assets/51871069/8a0ca94f-b3b2-4a27-bceb-179cba7100c6)

# Exxperiment 3: Transfer speed between 'UCSD' and 'SALT' : 

Using iperf3, Server Side :

``` 
-----------------------------------------------------------
Server listening on 5201
-----------------------------------------------------------
Accepted connection from 10.134.1.2, port 35338
[  5] local 10.134.129.2 port 5201 connected to 10.134.1.2 port 35348
[ ID] Interval           Transfer     Bitrate
[  5]   0.00-1.00   sec   163 MBytes  1.37 Gbits/sec                  
[  5]   1.00-2.00   sec   188 MBytes  1.58 Gbits/sec                  
[  5]   2.00-3.00   sec   188 MBytes  1.58 Gbits/sec                  
[  5]   3.00-4.00   sec   191 MBytes  1.60 Gbits/sec                  
[  5]   4.00-5.00   sec   186 MBytes  1.56 Gbits/sec                  
[  5]   5.00-6.00   sec   173 MBytes  1.45 Gbits/sec                  
[  5]   6.00-7.00   sec   143 MBytes  1.20 Gbits/sec                  
[  5]   7.00-8.00   sec   137 MBytes  1.15 Gbits/sec                  
[  5]   8.00-9.00   sec   112 MBytes   937 Mbits/sec                  
[  5]   9.00-10.00  sec  83.9 MBytes   704 Mbits/sec                  
[  5]  10.00-10.04  sec  2.77 MBytes   624 Mbits/sec                  
- - - - - - - - - - - - - - - - - - - - - - - - -
[ ID] Interval           Transfer     Bitrate
[  5]   0.00-10.04  sec  1.53 GBytes  1.31 Gbits/sec                  receiver
```

Client side : 
```
Connecting to host 10.134.129.2, port 5201
[  5] local 10.134.1.2 port 35348 connected to 10.134.129.2 port 5201
[ ID] Interval           Transfer     Bitrate         Retr  Cwnd
[  5]   0.00-1.00   sec   172 MBytes  1.45 Gbits/sec    0   6.05 MBytes       
[  5]   1.00-2.00   sec   185 MBytes  1.55 Gbits/sec    1   4.24 MBytes       
[  5]   2.00-3.00   sec   190 MBytes  1.59 Gbits/sec    0   4.24 MBytes       
[  5]   3.00-4.00   sec   189 MBytes  1.58 Gbits/sec    0   4.24 MBytes       
[  5]   4.00-5.00   sec   188 MBytes  1.57 Gbits/sec    1   3.00 MBytes       
[  5]   5.00-6.00   sec   174 MBytes  1.46 Gbits/sec    1   2.15 MBytes       
[  5]   6.00-7.00   sec   142 MBytes  1.20 Gbits/sec    0   2.27 MBytes       
[  5]   7.00-8.00   sec   134 MBytes  1.12 Gbits/sec    1   1.67 MBytes       
[  5]   8.00-9.00   sec   111 MBytes   933 Mbits/sec    1   1.59 MBytes       
[  5]   9.00-10.00  sec  85.0 MBytes   713 Mbits/sec    0   1.33 MBytes       
- - - - - - - - - - - - - - - - - - - - - - - - -
[ ID] Interval           Transfer     Bitrate         Retr
[  5]   0.00-10.00  sec  1.53 GBytes  1.32 Gbits/sec    5             sender
[  5]   0.00-10.04  sec  1.53 GBytes  1.31 Gbits/sec                  receiver

iperf Done.
```

On the same nodes I was measuring the throughput using sendpfast : Maximum I got was 58.7 Mb. 

![Screenshot from 2023-06-19 12-56-51](https://github.com/nagmat1/fabric_ethernet_througput_exp/assets/51871069/8d69a990-3dea-461f-b038-ce29fec09b06)






