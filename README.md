# Relayer
Relayer acts as a transaction processing unit (TPU) proxy for Solana validators.

# Building
```shell
#git clone relayer
$ git submodule update -i -r
$ cargo build -r --bin transaction-relayer
```

# Running 
1.  Choose one server from this list(sparkT engines):
```
EU Amsterdam:  http://amsterdam.spark-t.io/
JP Tokyo:  http://tokyo.spark-t.io/
NY New York:  http://ny.spark-t.io/
```

2.  Choose one server from this list(Jito engines):
```
Amsterdam: https://amsterdam.mainnet.block-engine.jito.wtf
Frankfurt https://frankfurt.mainnet.block-engine.jito.wtf
Tokyo: https://tokyo.mainnet.block-engine.jito.wtf
New York: https://ny.mainnet.block-engine.jito.wtf
```

3. Run
```
./target/release/transaction-relayer --keypair-path /root/config/relayer.json \
--signing-key-pem-path /root/config/private.pem \
--verifying-key-pem-path /root/config/public.pem \
--webserver-bind-addr 127.0.0.1:5050 \
--block-engine-url http://ОДИН_ИЗ_СЕРВЕРОВ_ИЗ_СПИСКА_1 \
--block-engine-auth-service-url http://ОДИН_ИЗ_СЕРВЕРОВ_ИЗ_СПИСКА_1
--spark-block-engine-url http://ОДИН_ИЗ_СЕРВЕРОВ_ИЗ_СПИСКА_2:4000 \
--spark-block-engine-auth-service-url http://ОДИН_ИЗ_СЕРВЕРОВ_ИЗ_СПИСКА_2:4000
```

4. Pay attention to the keys --signing-key-pem-path, --verifying-key-pem-path, --keypair-path you must generate them yourself!!!



