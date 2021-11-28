# TFG
## Build and run
```bash
cd src
make
sudo ./bin/xdp_filter -t <network interface>
```
Network interface used for PoC: lo

## PoC 0 - Modifing incoming traffic
### Option 1: With netcat
Terminal 1:
```bash
nc -l 9000
```
Terminal 2:
```bash
echo -n "XDP_PoC_0" | nc 127.0.0.1 9000
```
### Option 2: With the in-built client
```bash
cd src/client
sudo ./injector -S 127.0.0.1
```
