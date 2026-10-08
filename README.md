<p align="center">
  <a href="https://github.com/lpconsole/lp-music/releases"><img src="https://img.shields.io/badge/Version-0.2.9-blue.svg" alt="Version"></a>
    <a href="https://developer.android.com"><img src="https://img.shields.io/badge/Platform-Android-green.svg" alt="Platform"></a>
    <a href="#"><img src="https://img.shields.io/badge/License-All%20Rights%20Reserved-red.svg" alt="License"></a>
</p>

Reklamsiz TV ve radyo oynatici. Android TV ve kumanda kullanimi icin tasarlandi; WebView degildir, native Android uygulamasidir.

## Ozellikler

- IPTV kanallari `iptv-org` verilerinden yuklenir.
- Radyo kanallari Radio Browser API uzerinden yuklenir.
- TV ve radyo listeleri ayri sekmelerde tutulur.
- Favoriler desteklenir.
- Kanal sirasi uygulama icinden degistirilip kaydedilebilir.
- Radyo modunda hareketli poster GIF arka plani kullanilir.
- Uygulama ici guncelleme kontrolu icin manifest tabanli sistem hazirdir.
- Reklam, hesap, takip ve analitik yoktur.

## Guncelleme Sistemi

Uygulama `update.json` formatinda bir manifest okur:

GitHub repo acildiktan sonra en pratik yol:

- APK dosyasini GitHub Releases'a yuklemek.
- `update.json` dosyasini ayni release asset'i olarak yayinlamak.
- Uygulamadaki update URL'si `https://github.com/lpconsole/mediator/releases/latest/download/update.json` adresini okur.

indir -> [https://github.com/lpconsole/mediator/releases/download/latest/app-release.apk
](https://github.com/lpconsole/mediator/releases/latest/download/app-release.apk)

Android guncelleme icin tum surumler ayni keystore ile imzalanmalidir.

## Kaynaklar

- TV veri kaynagi: `https://iptv-org.github.io`
- Radyo veri kaynagi: `https://www.radio-browser.info`

Bu uygulama kendi icerigini barindirmaz; public API'lerden gelen stream adreslerini oynatir.
