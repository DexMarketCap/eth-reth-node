# Clone your fork locally
```
git clone https://github.com/yourusername/reth.git
cd reth
```

# Add upstream temporarily
```
git remote add upstream https://github.com/paradigmxyz/reth.git
```

# Fetch updates
```
git fetch upstream
```

# Update your MAIN branch with upstream changes
```
git checkout main
git fetch upstream
git merge upstream/main --ff-only 
git merge sven -m "Merge customizations from sven branch into main"
```

# Update your CUSTOM branch with upstream changes
```
git checkout sven
git merge main --ff-only

// 'git reset --hard main'
```

# Push Everything Safely
```
git push origin main
git push origin sven
```

# Custom method
rpc -> rpc-eth-api -> core.rs - Custom RPC methods trait + implementations
rpc -> rpc-eth-api -> helpers - functions


# local testing - testnet
```
cargo build --release

.\target\release\reth node --chain sepolia --http --http.addr 0.0.0.0
```