# Install Allora Worker Node
### 1. Stop and remove your worker:
#### - Worker3:
```Bash
cd worker3-20m && docker compose down
```
```Bash
cd
rm -rf worker3-20m
```
### 2. Clone repository:
```Bash
cd
git clone https://github.com/nhunamit/basic-coin-prediction-node.git
```
```Bash
mv basic-coin-prediction-node worker3-20m
cd worker3-20m
```
```Bash
git branch -a
git checkout worker3-20m
```
### 3. Edit file `nano config.json`
```Bash
nano config.json
```
Edit `"addressRestoreMnemonic"` change `just clap slim ...` by your mnemonic.
(Ctrl + X, Y and Enter will do to save)
### 4. Configuration:
```Bash
./init.config
```
### 5. Run:
```Bash
docker compose up -d
```
```Bash
docker compose logs -f
```

## Done!
---------------------------------------------------------------------------------------------

# Update Allora Worker Node
### 1. Stop your worker:
#### - Worker1:
```Bash
cd worker1-10m && docker compose down
```
#### - Worker2:
```Bash
cd worker2-24h && docker compose down
```
#### - Worker3:
```Bash
cd worker3-20m && docker compose down
```
### 2. Edit file `docker-compose.yml`
```Bash
nano docker-compose.yml
```
Edit file `config.json` as in the code below. 
(Ctrl + X, Y and Enter will do to save)

`image: alloranetwork/allora-offchain-node:latest`
### 3. Edit file `nano config.json`
```Bash
nano config.json
```
Edit file `config.json` as in the code below. 
(Ctrl + X, Y and Enter will do to save)

`"gas": "auto",`

`"gasAdjustment": 1.5,`

`"submitTx": true`
#### - Change your RPC (Option):
"nodeRpc": "your-new-RPC",
### 4. Configuration file:
```Bash
./init.config
```
### 5. Get latest image:
```Bash
docker compose pull
```
### 6. Rerun the worker:
```Bash
docker compose up -d --build
```
### 7. Check the worker log
```Bash
docker compose logs -f
```

## ----------------------Done---------------------


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

