FROM rust:1-slim AS builder
WORKDIR /app
COPY Cargo.toml .
COPY src ./src
RUN cargo build --release

FROM debian:stable-slim
COPY --from=builder /app/target/release/rust-app /usr/local/bin/rust-app
CMD ["rust-app"]
