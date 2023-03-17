# Find the ID of your current Docker Container.

```
docker ps
```

![image](https://user-images.githubusercontent.com/101462877/219213845-25d7cb76-9934-4899-916c-2138c992aeac.png)

For example here Container ID is `c8d967d14d5b`

# Stop and delete the current Docker Container with the commands below.

```
docker stop <CONTAINERID>
```
Example: `docker stop c8d967d14d5b`

```
docker rm <CONTAINERID>
```
Example: `docker rm c8d967d14d5b`



# Then run the run command with the latest version. Don't forget to replace the `<L1URL>` part with the `https` part that you copied from Alchemy.

```
docker run -d -v ~/data/arbitrum:/home/user/.arbitrum -p 0.0.0.0:8547:8547 -p 0.0.0.0:8548:8548 offchainlabs/nitro-node:v2.0.11-8e786ec -- l1.url <L1URL> --l2.chain-id=42161 --http.api=net,web3,eth,debug --http.corsdomain=* --http.addr=0.0.0.0 --http.vhosts= * --init.url="https://snapshot.arbitrum.io/mainnet/nitro-recent.tar"
```

# Get your new Docker Container ID for log checking.

```
docker ps
```

# Check the logs.

```
docker logs -f <CONTAINERID>
```
