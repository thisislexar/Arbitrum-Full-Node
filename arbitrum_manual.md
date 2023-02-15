# Sunucu güncelleyip docker yükleyin.

```
sudo apt update && sudo apt upgrade -y
sudo apt install docker.io -y
```

# Arbi klasörü açıp izin verin.

```
mkdir -p ~/data/arbitrum
chmod -fR 777 ~/data/arbitrum
```

# Run komutunu çalıştırın. `<L1URL>` kısmını Alchemy'den kopyaladığınız `https` kısmıyla değiştirmeyi unutmayın.

```
docker run -d -v ~/data/arbitrum:/home/user/.arbitrum -p 0.0.0.0:8547:8547 -p 0.0.0.0:8548:8548 offchainlabs/nitro-node:v2.0.11-8e786ec --l1.url <L1URL> --l2.chain-id=42161 --http.api=net,web3,eth,debug --http.corsdomain=* --http.addr=0.0.0.0 --http.vhosts=* --init.url="https://snapshot.arbitrum.io/mainnet/nitro.tar"
```
