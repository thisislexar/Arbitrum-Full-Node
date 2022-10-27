<h1 align="center">Arbitrum Full Node Kurulum Rehberi

## Olası bir Arbitrum airdrop'unda claim işlemlerinde sorun yaşamak istemiyorsanız, bu rehber sizin için🙂 Sağ üstten yıldızlayıp forklamayı unutmayalım. Sorularınız olursa: [LossNode Chat](https://t.me/LossNode)

![image](https://user-images.githubusercontent.com/101462877/198357079-6320f62f-8e9e-401d-becf-8673480e8701.png)

## Sistem gereksinimleri:
NODE TİPİ | CPU     | RAM      | SSD     |
| ------------- | ------------- | ------------- | -------- |
| Mainnet | 6          | 8         | 400-500  |

## Arbitrum için önemli linkler:
- [Website](https://arbitrum.io/)
- [Explorer](https://arbiscan.io)
- [Twitter](https://twitter.com/arbitrum)
- [Discord](https://discord.gg/arbitrum)

# 1) Node kurmadan önce Alchemy üzerinden endpoint alalım.

![image](https://user-images.githubusercontent.com/101462877/198358298-d6be4399-154d-4873-bc8c-e6f37db80860.png)

## [Alchemy](https://dashboard.alchemy.com/) üzerinde hesabınız yoksa hesap açıp `Create App` diyoruz.

![image](https://user-images.githubusercontent.com/101462877/198358599-14a29270-fd3d-4654-9f0d-503faa7992b2.png)

## Bir isim girip `Create App` diyelim.

![image](https://user-images.githubusercontent.com/101462877/198358754-a9f2f648-4895-429a-aa73-e240a3fcfe5e.png)

## Oluşturduğumuz App için `View key`'e tıklayalım.

![image](https://user-images.githubusercontent.com/101462877/198359002-9c032e82-7071-4a06-9868-0d6343f6dada.png)

## Açılan kısımda `https` kısmını kopyalayalım.


# 2) Node'u kuralım.

## 2a) Script ile kurulum.

``` 
wget -O arbitrum.sh https://raw.githubusercontent.com/thisislexar/Arbitrum-Full-Node/main/arbitrum.sh && chmod +x arbitrum.sh && ./arbitrum.sh
```
![image](https://user-images.githubusercontent.com/101462877/198361610-ff82d18b-9ca6-41be-8b7e-fc5381b5869e.png)

## `L1URL`'nizi girin dediği yerde Alchemy'den kopyaladığınız `https` kısmını giriyorsunuz.

## 2b) Manuel kurulum.

Node bilginizi geliştirmek adına dilerseniz [Manuel Kurulum](https://github.com/thisislexar/Arbitrum-Full-Node/blob/main/arbitrum_manual.md) da yapabilirsiniz.

## 3) Node loglarını kontrol.

Aşağıdaki komut ile docker container id'yi öğrenin.

``` 
docker ps
```
![image](https://user-images.githubusercontent.com/101462877/198364892-af160efa-66b2-4929-9e14-c79ea28b456a.png)

Ardından aşağıdaki komutla logları kontrol edin. <ID> kısmını bir üstteki görseldeki Container Id olarak değiştirin.

``` 
docker logs -f <ID>
```
![image](https://user-images.githubusercontent.com/101462877/198365298-62ee6d4c-e9c8-4290-af7c-e02ee4ab7667.png)


## 4) Node'unuz bir süre içerisinde sync olduktan sonra, metamask'e ekleme.

![image](https://user-images.githubusercontent.com/101462877/198362714-e6be4fa7-d750-4d5f-815a-77c129061f94.png)

## `Manuel ağ ekle`'ye tıklıyoruz. 

![image](https://user-images.githubusercontent.com/101462877/198363067-4ca01c95-f05c-47d5-997d-8177fb26e66c.png)

- `Ağ adı`: Fark etmez


- `RPC URL`: "http://" + SUNUCU IP'niz + ":8547" şeklinde. Yukarıdaki görselde de görebilirsiniz


- `Zincir Kimliği`: 42161


- `Para Birimi Sembolü`: ETH olsun

- `Explorer`: https://arbiscan.io

# Sorularınız ve merak ettikleriniz için: [LossNode Chat](https://t.me/LossNode)
