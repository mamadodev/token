# Use the official Rust dev container as the base image
FROM mcr.microsoft.com/vscode/devcontainers/rust:latest

# Install Node.js using NVM
RUN curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
ENV NVM_DIR="/root/.nvm"
RUN . "$NVM_DIR/nvm.sh" && nvm install --lts

# Install Solana CLI
RUN sh -c "$(curl -sSfL https://release.solana.com/stable/install)"
# Add Solana to PATH (adjust if needed)
ENV PATH="/root/.local/share/solana/install/active_release/bin:${PATH}"

# Install Anchor CLI from GitHub
RUN cargo install --git https://github.com/project-serum/anchor anchor-cli --locked
