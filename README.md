# Mining Ore on Windows 10/11 Unsing CLI


 All credits to @HardfHatChad for building Ore and the Ore-CLI
 
 Learn more about the Ore Project and HardHatChad
- https://ore.supply/
- https://twitter.com/OreSupply
- https://twitter.com/HardhatChad
- https://github.com/HardhatChad

# Things You Need
1. Ore CLI Miner
2. Rustup/Cargo
3. Solana CLI wallet
4. 0.01-0.02 SOL
5. Free RPC "Paid preferred" 


# Links

RustUp: https://rustup.rs/

SolanaCLI: https://docs.solanalabs.com/cli/install

Ore Website: https://ore.supply/downloads


# Start Building #

# 1. Install RustUp 

- open a terminal
$ curl https://sh.rustup.rs -sSf | sh
- close or refresh terminal


# 1.5. "may not have to do" Do anyways for 0 failers

$ sudo apt-get install openssl pkg-config libssl-dev
- close the terminal


# 2. Install Solana CLI (if already done skip to #5)
 
- open terminal
$ sh -c "$(curl -sSfL https://release.solana.com/v1.18.4/install)"
- check the version  
$ solana --version


# 3. Create And Back Up Wallet 

- create the wallet  
$ solana-keygen new

- save the Recovery phrase and password
- goto your keypair folder it told you "home/YOUR_USER/.config/solana/id.json"
- open and copy the id.json " import that into phantom wallet for easy tracking"


# 4. Install Ore-CLI 

- open terminal and run  
$ cargo install ore-cli


# 5. Top Up Wallet

- get your address  
$ Solana address

- send 0.01-0.02 SOL here


# 6. Get Your RPC

- goto the RPC link and create a account
- copy your free rpc api  


# 7. Start Mining Ore

  ore --rpc "your free or paid RPC" --keypair home/YOUR_USER/.config/solana/id.json --priority-fee 10000 mine --cores " your PC core count, run one less for better stability"
  
- change the keypair location to your that you saved from step 5


# Helpful Commands

Check ORE Rewards"unclaimed":  
$ ore --keypair C:\Users\ "keypair location"\.config\solana\id.json rewards

Check ORE Balance"claimed":  
$ ore --keypair C:\Users\ "keypair location"\.config\solana\id.json balance

Claim ORE Rewards:  
- you can run this a a batch but watch closly for a claim so you can stop the batch  
$ ore --rpc "your free or paid RPC" --keypair C:\Users\ "keypair location"\.config\solana\id.json --priority-fee 5000 claim

Check SOL Balance:   
$ solana balance

Check SOL Address:  
$ solana address

Import A SOL Seed Phrase:  
$ solana-keygen recover
