# XenBlocksP2PGuide
Follow this guide to test the XenBlocks P2P Network 

| Command | Description |
|---------|-------------|
| `go version` | Verify version of Go (if installed) |
| `sudo rm -rf /usr/local/go` | Remove old version (optional) |
| `uname -m` | Check system architecture |
| `wget https://go.dev/dl/go1.21.3.linux-amd64.tar.gz` | Download new version |
| `sudo tar -C /usr/local -xzf go1.21.3.linux-amd64.tar.gz` | Extract tarball (compressed file) |
| `nano ~/.bashrc` | Open `~/.bashrc` file for editing |
|  `export PATH=$PATH:/usr/local/go/bin` <br> `export GOPATH=$HOME/go` <br> `export PATH=$PATH:$GOPATH/bin` | Add the following lines to the end of the file to set Go environment variables  |
| `source ~/.bashrc` | Reload profile to apply changes |
| `go version` | Verify new version of Go |
| `git clone https://github.com/FairCrypto/xenminer-p2p` | Clone XenMiner P2P GitHub repository |
| `cd xenminer-p2p` | Change directory to xenminer-p2p folder |
| `go mod init p2p` | Initialize new module (replace `[module name]` with the actual name) |
| `go mod tidy` | Update Go projects |
| `go mod verify` | Verify Go projects |
| `go run *.go --log info --roles rpc,miner` | Run P2P Test |
