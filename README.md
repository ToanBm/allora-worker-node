# allora-worker-node

## 1. Configuration requirements
```Bash
Operating System: Ubuntu.
CPU: 1-2 core.
Memory: 2-3 GB.
Storage: SSD or NVMe with at least 50GB of space.
```
## 2. 2. Install tool and create worker wallet
```Bash
curl -sSL https://raw.githubusercontent.com/allora-network/allora-chain/main/install.sh | bash -s -- v0.3.0
```
```Bash
nano ~/.bashrc
```

```Bash
export PATH="$PATH:/root/.local/bin"

```Bash
source ~/.bashrc

```Bash
allorad keys add net1_worker

