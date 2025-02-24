# CLI Node Run Full Guide (PC)

### Offical Docs by Pipe Network - https://docs.pipe.network/devnet-2

1️⃣ Dependencies for WINDOWS & LINUX
```
sudo apt update
sudo apt upgrade -y
```

2️⃣ Download Some Files
```
curl -L -o pop "https://dl.pipecdn.app/v0.2.8/pop"
```
```
chmod +x pop
```

3️⃣ Make Directory (create folder to be used for download cache)
```
mkdir download_cache
```

4️⃣ Signup Your Account
```
./pop --signup-by-referral-route 332de39758d724e9
```

```
# Generate Your Referral
./pop --gen-referral-route
```

5️⃣ Start Node
````
sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY>
```
                                                            OR   (Recommended Phantom Wallet or ANY SOL Wallet)

sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY>--enable-80-443
````
# Open Another Window for WSL or VPS

## Save the file
```
nano ~/node_info.json
```

## Monitor your Node Status & Points
```
./pop --status
```
```
./pop --points
```

## Check Points & Status from Dashboard - https://dashboard.pipenetwork.com/node-lookup


## 🔶For Next Day Run This Command

#1 Open WSL and Put this Command 
```
sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY>
```

Note: Replace your `ram` , `disk` & `pubkey` with your actual Information.Retrieve the public key from your Solana wallet (e.g., Phantom, Backpack)

## Upgrade Your Node in v0.2.8

1️⃣ Upgrade (Download Latest Version)
```
curl -L -o pop "https://dl.pipecdn.app/v0.2.8/pop"
```
```
chmod +x pop
```

2️⃣ Start Node
```
sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY>
```

Note: Put your `ram` , `disk` & `pubkey` with your actual Information.Retrieve the public key from your Solana wallet (e.g., Phantom, Backpack) & Replace in `<KEY>` by Solana Address

## Need to Free Your 8003 Port

### Identify the Process Using Port 8003
```
sudo ss -tulpn | grep 8003
```

Example - ``` LISTEN  0  128  0.0.0.0:0380  0.0.0.0:*  users:(("nginx",pid=1234,fd=6)) ```

### Terminate the Process by PID
```
sudo kill -9 1234
```

### Kill All Processes Using Port 8003
```
sudo fuser -k 8003/tcp
```