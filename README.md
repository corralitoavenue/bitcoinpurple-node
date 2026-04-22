# BitcoinPurple Core (Integration / Staging Tree)

This repository contains the official full node implementation of BitcoinPurple.

BitcoinPurple is a decentralized cryptocurrency based on the Bitcoin protocol, designed to provide fast, secure, and low-cost transactions while preserving the core principles of decentralization and security.

---

## ⚙️ Build Instructions

To compile the node from source:

```bash
./autogen.sh
./configure
make
```

---

## 🚀 Running the Node

After compilation, the daemon can be started from the `src` directory.

```bash
./bitcoinpurpled
```

---

## ⚙️ Configuration

The node is configured via a standard configuration file.

### 1. Create Configuration File

Create a file named `bitcoinpurple.conf`:

```ini
# Performance
dbcache=512
maxmempool=300
maxconnections=64

# RPC settings
rpcuser=bitcoinpurpleuser
rpcpassword=strongpassword
rpcport=RPC_PORT
rpcbind=127.0.0.1
rpcallowip=127.0.0.1

# Network
port=P2P_PORT
listen=1
server=1

# Data directory
datadir=/path/to/your/datadir

# ZMQ
zmqpubhashblock=tcp://127.0.0.1:28332

# Peer nodes
addnode=node3.walletbuilders.com
addnode=172.77.254.247
addnode=176.116.187.125
addnode=185.210.226.109
addnode=185.250.240.81
addnode=185.250.243.159
addnode=196.133.152.35
addnode=2.56.245.17
addnode=31.207.228.208
addnode=35.144.68.73
addnode=45.131.66.138
```

> Replace `RPC_PORT` and `P2P_PORT` with the correct values for your deployment.

---

### 2. Start the Node

```bash
./bitcoinpurpled -conf=/path/to/bitcoinpurple.conf
```

---

## 🔧 Features

### 🔹 Proof of Work (SHA-256)
BitcoinPurple uses the SHA-256 Proof of Work algorithm, compatible with ASIC mining hardware.

---

### 🔹 Fast Block Time
BitcoinPurple is designed with a **target block time of 1 minute**, enabling fast transaction confirmations.

---

### 🔹 Fixed Supply
The total supply is capped at **1,000,000 BTCP**, ensuring long-term scarcity.

---

### 🔹 Fair Launch
BitcoinPurple launched with no premine, ensuring fair and transparent distribution from the genesis block.

- Initial block reward: **1 BTCP**
- Halving interval: **500,000 blocks**
- Current block reward: **0.25 BTCP (approx., depending on network height)**

### 🔹 Coinbase Maturity
Mining rewards require **100 confirmations** before being spendable.

---

### 🔹 Difficulty Adjustment
BitcoinPurple includes a dynamic difficulty adjustment mechanism to maintain stable block production under varying network conditions.

---

## 📄 Notes

- Ensure your node is fully synced before use.  
- Keep RPC credentials secure.  
- Open required ports if running a public node.  
- Always use the latest official version.

---

## 📜 License

See the LICENSE file for details.
