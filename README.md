# mediator

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

## Test APK

Debug APK:

```text
app/build/outputs/apk/debug/app-debug.apk
```

Yerel derleme:

```powershell
$env:JAVA_HOME='C:\Program Files\Eclipse Adoptium\jdk-17.0.2'
cmd /c gradlew.bat assembleDebug --console=plain
```

## Guncelleme Sistemi

Uygulama `update.json` formatinda bir manifest okur:

```json
{
  "versionCode": 7,
  "versionName": "0.2.1",
  "apkUrl": "https://github.com/lpconsole/mediator/releases/latest/download/mediator-v0.2.1.apk",
  "notes": "Yeni surum"
}
```

GitHub repo acildiktan sonra en pratik yol:

- APK dosyasini GitHub Releases'a yuklemek.
- `update.json` dosyasini ayni release asset'i olarak yayinlamak.
- Uygulamadaki update URL'si `https://github.com/lpconsole/mediator/releases/latest/download/update.json` adresini okur.

Android guncelleme icin tum surumler ayni keystore ile imzalanmalidir.

## Kaynaklar

- TV veri kaynagi: `https://iptv-org.github.io`
- Radyo veri kaynagi: `https://www.radio-browser.info`

Bu uygulama kendi icerigini barindirmaz; public API'lerden gelen stream adreslerini oynatir.
