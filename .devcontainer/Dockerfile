FROM rust:1.77.0-slim-bookworm

WORKDIR /usr/src/myapp

RUN apt-get -qq update \
    && apt-get -qqy --no-install-recommends install \
    curl \
    apt-utils \
    pkg-config \
    libssl-dev

# wasm-pack is your one-stop shop for building, testing, and publishing Rust-generated WebAssembly.
RUN curl https://rustwasm.github.io/wasm-pack/installer/init.sh -sSf | sh

# cargo-generate helps you get up and running quickly with a new Rust project by leveraging a pre-existing git
# repository as a template.
RUN cargo install cargo-generate
