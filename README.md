
# 🎛 PIPE CLI Node In-Depth Guide

### 📚 Official Docs by Pipe Network
[Pipe Network Docs](https://docs.pipe.network/devnet-2)

---

## ⚙️ Dependencies for WINDOWS & LINUX
```sh
sudo apt update && sudo apt upgrade -y
```

## 📥 Download Some Files
```
curl -L -o pop "https://dl.pipecdn.app/v0.2.8/pop"

```
## For background run
```
chmod +x pop
```

## 📂 Make Directory (create folder to be used for download cache)
```
mkdir download_cache
```

## 📝 Signup Your Account
```
./pop --signup-by-referral-route 332de39758d724e9
```
# Generate Your Referral (Optional)
```
./pop --gen-referral-route
```

## 🚀 Start Node
```
sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY>
```
# OR (Recommended Phantom Wallet or ANY SOL Wallet)
```
Use this commnd only if your 8003 PORT is disable or got any error while last cmmnd (Optional)
```
sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY> --enable-80-443
```
**🔔 Important Note:** Replace your `ram`, `disk`, & `pubkey` with your actual information. Retrieve the public key from your Solana wallet (e.g., Phantom, Solflare, Backpack, etc.)
---

## 🌐 Open Another Window for WSL or VPS

### 💾 Save the file
```
nano ~/node_info.json
```

### 🔍 Monitor your Node Status & Points
```
./pop --status
```
### 🔍 Monitor your Node Points
``` 
./pop --points
```

### 🖥 Check Dashboard Here
[Pipe Network Dashboard](https://dashboard.pipenetwork.com/node-lookup)

---

## 🔄 For re-run, Run This Command

### 1️⃣ Open WSL and Paste it
```
sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY>
```

**🔔 Important Note:** Replace your `ram`, `disk`, & `pubkey` with your actual information. Retrieve the public key from your Solana wallet (e.g., Phantom, Solflare, Backpack, etc.)

---

## ⬆️ Upgradation

### 1️⃣ Upgrade (for Latest Version)
```
curl -L -o pop "https://dl.pipecdn.app/v0.2.8/pop"
```
 After that use it
 ```
chmod +x pop
```

### 2️⃣ Start Node
```
sudo ./pop --ram 8 --max-disk 500 --cache-dir /data --pubKey <KEY>
```

**🔔 Important Note:** Replace your `ram`, `disk`, & `pubkey` with your actual information. Retrieve the public key from your Solana wallet (e.g., Phantom, Solflare, Backpack, etc.)

---

## 🔓 Need to Free Your 8003 Port

### 🔍 Identify the Process Using Port 8003
```
sudo ss -tulpn | grep 8003
```

Example:
```
LISTEN  0  128  0.0.0.0:0120  0.0.0.0:*  users:(("nginx",pid=0120,fd=6))
```

### 🛑 Terminate the Process by PID
```
sudo kill -9 0120
```

### 🗑 Kill All Processes Using Port 8003
```
sudo fuser -k 8003/tcp
```

---

🎉 **Now Feel free & Enjoy your Node is running successfully**

```

Feel free to adjust any part of this to better suit your needs! If you need further tweaks or additions, just let me know.
```
