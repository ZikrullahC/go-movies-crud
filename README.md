# Film Kütüphanesi API

Bu proje, Go dilinde yazılmış basit bir RESTful API örneğidir. Gorilla Mux router'ını kullanarak filmler üzerinde temel CRUD işlemlerini gerçekleştiren bir HTTP sunucusu oluşturur.

## Başlarken

Bu talimatlar, projenizi yerel makinenizde çalıştırmak ve geliştirmek için bir kopya almanıza yardımcı olacaktır. Dağıtım notları, canlı bir sistemde nasıl çalıştırılacağına dair notları içerir.

### Önkoşullar

Bu projeyi çalıştırmak için aşağıdaki araçların yüklü olması gerekmektedir:

- Go (1.15 veya daha yeni)
- Gorilla Mux
- RS CORS

### Kurulum

Projeyi yerel makinenize klonlayın:

``` bash
https://github.com/ZikrullahC/go-movies-crud.git
```


Bağımlılıkları indirin ve kurun:

``` bash
go get -u github.com/gorilla/mux 
```

``` bash
go get -u github.com/rs/cors
```



### Çalıştırma

Sunucuyu başlatmak için:


Varsayılan olarak, sunucu 9090 numaralı portta çalışacaktır.

## API Kullanımı

API, aşağıdaki endpoint'leri sunar:

- `GET /movies`: Mevcut tüm filmleri listeler.
- `GET /movies/{id}`: Belirli bir ID'ye sahip filmi getirir.
- `POST /movies`: Yeni bir film oluşturur.
- `PUT /movies/{id}`: Belirli bir ID'ye sahip filmi günceller.
- `DELETE /movies/{id}`: Belirli bir ID'ye sahip filmi siler.

## Yapılandırma

Sunucu portunu değiştirmek için, `main.go` dosyasındaki `http.ListenAndServe` fonksiyonunu düzenleyin:

```go
http.ListenAndServe(":8080", handler)

