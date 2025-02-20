FROM mcr.microsoft.com/devcontainers/rust:latest

RUN apt-get update && apt-get install -y curl

# Install Solana CLI
RUN   sh -c "$(curl -sSfL https://release.anza.xyz/v2.1.13/install)"
ENV PATH="/root/.local/share/solana/install/active_release/bin:${PATH}"

# Install Anchor
RUN cargo install --git https://github.com/coral-xyz/anchor anchor-cli --locked
