<h1 align="center">Arbitrum Full Node Installation Guide

## If you don't want to having problems with claim for a possible Arbitrum airdrop, this guide is for you. Do not forget to star and fork from the top right. If you have questions: [LossNode Chat](https://t.me/LossNode)

![image](https://user-images.githubusercontent.com/101462877/198357079-6320f62f-8e9e-401d-becf-8673480e8701.png)

## System Requirements:
NODE TYPE | CPU     | RAM      | SSD     |
| ------------- | ------------- | ------------- | -------- |
| Mainnet | 6          | 8         | 400-500  |

## Important links for Arbitrum:
- [Website](https://arbitrum.io/)
- [Explorer](https://arbiscan.io)
- [Twitter](https://twitter.com/arbitrum)
- [Discord](https://discord.gg/arbitrum)

# 1) Before installing node, get your endpoint from Alchemy.

![image](https://user-images.githubusercontent.com/101462877/198358298-d6be4399-154d-4873-bc8c-e6f37db80860.png)

## If you do not have an account on [Alchemy](https://dashboard.alchemy.com/), open an account and click `Create App`.

![image](https://user-images.githubusercontent.com/101462877/198358599-14a29270-fd3d-4654-9f0d-503faa7992b2.png)

## Enter a name and click `Create App`.

![image](https://user-images.githubusercontent.com/101462877/198358754-a9f2f648-4895-429a-aa73-e240a3fcfe5e.png)

## Click `View key` for the App you created.

![image](https://user-images.githubusercontent.com/101462877/198359002-9c032e82-7071-4a06-9868-0d6343f6dada.png)

## Copy the `https` part in the opened section.


# 2) Install the Arbitrum node.

## 2a) Scripted installation.

``` 
wget -O arbitrumEN.sh https://raw.githubusercontent.com/thisislexar/Arbitrum-Full-Node/main/arbitrumEN.sh && chmod +x arbitrumEN.sh && ./arbitrumEN.sh
```
![image](https://user-images.githubusercontent.com/101462877/198361610-ff82d18b-9ca6-41be-8b7e-fc5381b5869e.png)

## Enter the `https` part you copied from Alchemy when it asks for `L1URL`

## 2b) Manual installation.

You can also install the node [manually](https://github.com/thisislexar/Arbitrum-Full-Node/blob/main/arbitrum_manualEN.md) to improve your Node knowledge.

## 3) Check your logs.

Learn Docker Container ID with following command.

``` 
docker ps
```
![image](https://user-images.githubusercontent.com/101462877/198364892-af160efa-66b2-4929-9e14-c79ea28b456a.png)

After that, check your node logs. Change `<ID>` part with the Container ID that you obtained from the command above.

``` 
docker logs -f <ID>
```
![image](https://user-images.githubusercontent.com/101462877/198365298-62ee6d4c-e9c8-4290-af7c-e02ee4ab7667.png)


## 4) Adding your node rpc url to metamask after node installation.

![image](https://user-images.githubusercontent.com/101462877/198362714-e6be4fa7-d750-4d5f-815a-77c129061f94.png)

## Click `add network manually`.

![image](https://user-images.githubusercontent.com/101462877/198363067-4ca01c95-f05c-47d5-997d-8177fb26e66c.png)

- `Network Name`: Does not matter


- `RPC URL`: "http://" + your server IP + ":8547" (As seen from the above picture)


- `Chain ID`: 42161


- `Currency`: Say ETH

- `Explorer`: https://arbiscan.io

# If you have any question: [LossNode Chat](https://t.me/LossNode)
