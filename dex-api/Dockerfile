FROM rust:1.58 as builder

WORKDIR /usr/src/xcaddex-api
COPY . .
RUN cargo install diesel_cli --no-default-features --features postgres --path .

FROM debian:buster-slim
RUN apt-get update && apt-get install -y extra-runtime-dependencies && rm -rf /var/lib/apt/lists/*
COPY --from=builder /usr/local/cargo/bin/xcaddex-api /usr/local/bin/xcaddex-api
CMD ["xcaddex-api"]