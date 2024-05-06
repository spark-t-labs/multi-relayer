# Relayer
Relayer acts as a transaction processing unit (TPU) proxy for Solana validators.

# Building
```shell
#git clone relayer
$ git submodule update -i -r
$ cargo build -r --bin transaction-relayer
```

# Running 
1.  Choose one server from this list:
```
EU Amsterdam:  http://amsterdam.spark-t.io/
```

2. Run
```
./target/release/transaction-relayer --keypair-path /root/config/relayer.json \
--signing-key-pem-path /root/config/auth \
--verifying-key-pem-path /root/config/auth.pub \
--webserver-bind-addr 127.0.0.1:5050 \
--block-engine-url http://ОДИН_ИЗ_СЕРВЕРОВ_ИЗ_СПИСКА_2:11227 \
--block-engine-auth-service-url http://ОДИН_ИЗ_СЕРВЕРОВ_ИЗ_СПИСКА_2:11227
```

4. Pay attention to the keys --signing-key-pem-path, --verifying-key-pem-path, --keypair-path you must generate them yourself!!!



