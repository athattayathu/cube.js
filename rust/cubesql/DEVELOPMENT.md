# Running in standalone mode

Prerequisites:

- `rustup`

```bash
rustup default nightly-2021-07-04
cd rust/cubesql
CUBESQL_CUBE_URL=$URL/cubejs-api \
CUBESQL_CUBE_TOKEN=$TOKEN \
CUBESQL_LOG_LEVEL=debug \
CUBESQL_BIND_ADDR=0.0.0.0:4444 \
cargo run

mysql -u root -h 127.0.0.1 --ssl-mode=disabled -u root --password=test --port 4444
```
