# Installation and Pre-requisites

- Install [Solana-CLI](https://docs.solana.com/cli/install-solana-cli-tools)
- Install [Rust](https://www.rust-lang.org/tools/install)
- Install Spl-Token-CLI using cargo
  - `cargo install spl-token-cli`

# List of Solana-CLI commands and their uses

- solana-keygen new
  - creates new wallet
- solana-keygen pubkey
  - displays public key of your wallet
- solana balance --url devnet
  - check balance of your account on devnet
- solana airdrop --url devnet [AMOUNT] [YOUR_ADDRESS]
  - receive test solana in your wallet

# List of Spl-Token CLI commands and their uses

- spl-token create-token --url devnet
  - create your own token using existing program library
  - ex : AT624CUm44dX69Q9e1kXzhgLYdrS8iSHDJ51S6CqKWep (custom token created using above command)
- spl-token create-account [CUSTOM_TOKEN_ADDRESS] --url devnet
  - creates the account to hold the custom token that we created
  - ex: 9WpuWuQ5QpAqTz8HxpQeCxPUdW8S6SqUSLdd5aHjdJJA (account created using the custom token address)
- spl-token balance [CUSTOM_TOKEN_ADDRESS] --url devnet
  - get balance of your custom token
- spl-token mint [CUSTOM_TOKEN_ADDRESS] [AMOUNT] --url devnet
  - mint test tokens to the account created for the custom token
- spl-token supply AT624CUm44dX69Q9e1kXzhgLYdrS8iSHDJ51S6CqKWep --url devnet
  - returns total supply for your custom token
- spl-token authorize mint [CUSTOM_TOKEN_ADDRESS] --disable --url devnet
  - revokes minting authority from the user and caps the amount of circulating tokens to the amount previously minted
- spl-token burn [CUSTOM_TOKEN_ACCOUNT_ADDRESS] [AMOUNT] --url devnet
  - burns the tokens from the token account
- spl-token transfer [CUSTOM_TOKEN_ADDRESS] [AMOUNT] [RECEIVER_CUSTOM_TOKEN_ACCOUNT_ADDRESS] --url devnet
  - transfers the given amount of tokens from the created-token address to the receiver's token account address
