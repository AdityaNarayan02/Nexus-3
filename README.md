## Nexus Testnet 3

# Install dependencies
```
sudo apt update && sudo apt upgrade -y
sudo apt install -y build-essential pkg-config libssl-dev git protobuf-compiler
```
## For VPS
```
sudo apt update
sudo apt install screen -y
```

## Install Rust
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source ~/.cargo/env
```

# Install cli
```
curl https://cli.nexus.xyz/ | sh
source ~/.bashrc
```

# Create a Screen Session (FOR VPS)
```
screen -s nexus
```

# Start the Node
```
nexus-network start --node-id <your-node-id>
```
#### To get the Node -ID

* Visit app.nexus.xyz and log in

* Navigate to Nodes → Add CLI Node

* Copy your Node ID

### You can also register with your wllet address & Start your Node
```
nexus-network register-user --wallet-address <YOUR_WALLET_ADDRESS>
nexus-network register-node
nexus-network start
```
## For VPS users
* To exit the screen session Press-> Ctrl+A+D
* TO see Node Logs/ To Join the screen session again
* ```
  Screen -r nexus
  ```
## If you face any issues regarding the installation, feel free to drop you issues here

  
