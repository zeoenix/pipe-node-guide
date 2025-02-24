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

## Check Dashboard Here - https://dashboard.pipenetwork.com/node-lookup


## 🔶 for re-run Run This Command

#1 Open WSL and Paste it 
```
sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY>
```

Important Note: Replace your `ram` , `disk` & `pubkey` with your actual Information. Retrieve the public key from your Solana wallet (e.g., Phantom, solfare, and Backpack etc.)

## Upgradation

1️⃣ Upgrade (for Latest Version)
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

Important Note: Replace your `ram` , `disk` & `pubkey` with your actual Information. Retrieve the public key from your Solana wallet (e.g., Phantom, solfare, and Backpack etc.)

                              ## Now Feelfree & Enjoy your Node is running successfully
