# Clone your fork locally
git clone https://github.com/yourusername/reth.git
cd reth

# Add upstream temporarily
git remote add upstream https://github.com/paradigmxyz/reth.git

# Fetch updates
git fetch upstream

# Update your MAIN branch with upstream changes
git checkout main
git merge upstream/main

# Update your CUSTOM branch with upstream changes
git checkout sven
git merge upstream/main
# Resolve conflicts, then:
git push origin sven

# push updates to branch
git add .
git commit -m "feat: my custom changes"
git push origin sven



# Custom method
rpc -> rpc-eth-api -> custom.rs - Custom RPC methods trait + implementations
rpc -> rpc-eth-api -> lib.rs - Import Mods

rpc -> rpc-eth-api -> core.rs - Core RPC methods trait + implementations