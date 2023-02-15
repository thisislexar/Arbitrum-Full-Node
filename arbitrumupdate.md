# Güncel Docker Container'ınızın ID'sini bulun.

```
docker ps
```

![image](https://user-images.githubusercontent.com/101462877/219213845-25d7cb76-9934-4899-916c-2138c992aeac.png)

Örneğin burada Container ID `c8d967d14d5b`

# Aşağıdaki komutlarla güncel Docker Container'ını durdurun ve silin.

```
docker stop <CONTAINERID>
```
Örnek: `docker stop c8d967d14d5b`

```
docker rm <CONTAINERID>
```
Örnek: `docker rm c8d967d14d5b`



# Ardından en güncel sürümle birlikte run komutunu çalıştırın. `<L1URL>` kısmını Alchemy'den kopyaladığınız `https` kısmıyla değiştirmeyi unutmayın.

```
docker run -d -v ~/data/arbitrum:/home/user/.arbitrum -p 0.0.0.0:8547:8547 -p 0.0.0.0:8548:8548 offchainlabs/nitro-node:v2.0.11-8e786ec --l1.url <L1URL> --l2.chain-id=42161 --http.api=net,web3,eth,debug --http.corsdomain=* --http.addr=0.0.0.0 --http.vhosts=* --init.url="https://snapshot.arbitrum.io/mainnet/nitro.tar"
```
