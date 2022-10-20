<h1 align="center"> Zeeka Network | The Chaos Testnet 1 </h1>

![image](https://user-images.githubusercontent.com/101149671/196880084-be318e37-979b-4c9e-bb14-5765ddcfc901.png)

<h1 align="center"> Selamlar, beklenen gün sonunda geldi.. Bu rehbere alışıla gelmişten farklı başlayacağım. Aramıza yeni katılanlar olduğunu düşünüyor ve en yalın hali ile anlatıyorum.. </h1>

### [Zeeka Network Telegram](https://t.me/ZeekaNetworkTurkish) - [Zeeka Network Discord](https://discord.gg/jbtvXSP3)

![image](https://user-images.githubusercontent.com/101149671/196889312-d1edc9bc-c0e3-4fd2-a3d1-15167c712dca.png)

# Öncelikle, yeni başladıysanız Node nedir? Sanal sunucu nedir? Nasıl kullanılır ve Sunucuya nasıl bağlanılır onları öğrenmelisiniz:

 * Sunucu ve Node Kurulumu Temel Bilgiler: [Link](https://is.gd/sunucuvenode)
 * Node Kurmak İstiyorum Nasıl Başlarım?: [Link](https://forum.rues.info/index.php?threads/node-kurmak-istiyorum-nasil-baslarim.2384/)
 * Daha fazla bilgi [discord kanalımda](discord.gg/ruescommunity) yeni başladım ve sunucu-node bilgileri odasında mevcut.
 * Sorularınız varsa: [Duyuru](https://t.me/RuesAnnouncement) - [Sohbet](https://t.me/RuesChat)
 * Şimdi sunucunuzu temin ettiyseniz node kurulumuna geçelim. Evet ödüllü..
 
## Gereksinimler:

 * Minimum gereksinimler yeterli olur
```
 2 CPU
 4 RAM
```

## Kurulum
```
sudo apt install -y build-essential libssl-dev cmake
```
```
apt install screen
```

## Rust toolunu kuruyoruz:

 * Kurulum esnasında 1 - 2 ve 3 seçenekleri çıkacak, 1'i seçiyoruz.

```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

![image](https://user-images.githubusercontent.com/101149671/196891892-ef3bb9b4-12f8-44fc-a062-7e008fa6c77a.png)


## Bazukayı yüklüyoruz:
```
apt install git
git clone https://github.com/zeeka-network/bazuka
```
```
source "$HOME/.cargo/env"
```
## path'ı kuruyoruz:
```
cd bazuka
cargo install --path .
```
## Burdan sonrası dikkatli okuyalım:

 * Bu komutta sadece `RUESSEED` dediğim yeri değiştirin ve bunu kaydedin, bu sizin seediniz
 * Nodu bir gün taşımak isterseniz bu `SEED` ile nodu kuracaksınız.

```
bazuka init --seed RUESSEED --network chaos --node 127.0.0.1:8765
```

## Şimdi nodumuzu farklı screende çalıştıralım:

```
screen -S bazuka
```

 * Burada 2 kısım değiştirelecek ve yeni açılan screen (pencere) içersine girilecek
 * Birinci kısım external kısmında ki `123.123.123` diye örnek verdiğim kısma IP numaranızı girin, sonda ki `8765` kalacak o port numarası.
 * İkinci kısım `--discord-handle "rues#1234"` discordunuzu girin, zeeka'nın discordunda olduğunuzdan emin olun.

```
bazuka node --listen 0.0.0.0:8765 --external 123.123.123:8765 \
  --network chaos --db ~/.bazuka-chaos --bootstrap 152.228.155.120:8765 \
  --discord-handle "rues#1234"
```

## Daha sonra görselde ki gibi çıktı alacaksınız:

 * active node sayısı 1-2-10-30-100 diye gözükecek
 * 0 gözükürse kurduktan bir kaç dakika sonra bana zeeka türkiye telegramdan yazın. (biraz beklemeyi unutmayın)

![image](https://user-images.githubusercontent.com/101149671/196894807-5a3b4890-b45c-46eb-9f5b-9c75be02c278.png)

* 0 gözükme örneği:

![image](https://user-images.githubusercontent.com/101149671/196895349-4abe0823-8449-41a1-bd9f-147e90c7fa2f.png)

## Zeeka hakkında:

  * [Explorer linki](http://152.228.155.120:8000/)
  * [Web Site](https://zeeka.network/)
  * [Twitter](https://twitter.com/ZeekaNetwork)

# Not: 

### Zeeka'nın discorduna ve twitterına dahil olmayı unutmayın, ha bu arada eğer bit github hesabınız yoksa kesin olsun.



