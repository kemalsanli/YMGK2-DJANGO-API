# YMGK2-DJANGO-API

[YMGK2](https://github.com/kemalsanli/YMGK2) projesinin sunucuda çalıştırılabilir hali.
Geliştirme süreci çok önce başlamış olmasına rağmen yayınlanmadan önce ayrı repoya ayrılmıştır.

## Açıklama

[YMGK2](https://github.com/kemalsanli/YMGK2) projesinin sunucuda çalışabilir hali, OTP'nin en büyük sorunlarından biri olan gizliliği korumak için anahtarı kullanıcının kendisine bile vermeyerek görüntüyü şifreler. Sistemin kullanıcıdan tek isteği görseldir, görselin şifreli mi şifresiz mi olduğunu tanır ve buna göre görselin açılması gerekiyorsa açar şifrelenmesi gerekiyorsa şifreler, kullanıcıya sağladığı rahatlık bir yana dursun anahtar cihaza uğramadığı için hem maliyetleri azaltır hem güvenliği artırır hem de tek seferlik şifreleme açma özelliği sayesinde ortadaki adam saldırılarında elde edilen şifreli görselin tekrar açılamamasını sağlar. 

Bu proje dersi geçmek için değil dijital dünyada son kullanıcının veri güvenliğini sağlamak için yapılmıştır, bu yüzden de son kullanıcıdan sadece görseli talep eder. Kullanıcı tecrübesi bu projenin kullanıcı güvenliği ve gizliliğinden sonra en çok önem verdiği şeydir.

## Başlarken

### Gereklilikler

* Python 3+
* pip
* Django


### Kurulum Gereksinimleri

* Curl kullanılabilir olmalıdır.

### Kurulum

* Pip kurulumu için gerekli olan get-pip.py dosyasını indirin.

```
curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
```
* Sonrasında pip kurulumunu başlatın. 

```
python get-pip.py
```
* Gerekli kütüphaneleri yükleyin. 

```
pip install opencv-python Pillow numpy
```

* Uygulamayı çalıştırmak için komut satırı üzerinde dosyaların bulunduğu klasöre gelip verilen komutu çalıştırın. 

```
python manage.py runserver
```
* Artık uygulamyı kullanmaya hazırsınız. 

* Opsiyonel olarak yazdığımız arayüzde sistemin nasıl çalıştığını görmek veya işlem yapmak için şu kodu girebilirsiniz.

```
python arayüz.py
```

## Yardım

Henüz herhangi bir sorunla karşılaşmadık.
```
...ama siz yine de sorun yaşarsanız bi kapatıp açın
```

## Kullanım

Formdata olarak image ve hash parametrelerini göndermelisiniz. 

Görsellerin bitwise olarak xor'lanabilmesi için hash değerleri önem arz etmektedir fakat eğer görseli sorunsuz açmak istiyorsanız görsel üzerinde oynama yapmamalısınız.

Hash değeri opsiyonel olmasa da zorunlu da değildir, yani aynı hash değeri ile farklı keyler üretebilirsiniz. Hash key üretilmesinde kullanılan faktörlerden sadece bir tanesidir. 

POST isteği göndereceğiniz adres şunun gibi olmalıdır:
```
http://127.0.0.1:8000/api/
```

## Arayüz

* Postman üzerinde örnek bir kullanım.

![POSTMAN 1](https://github.com/kemalsanli/YMGK2-DJANGO-API/blob/main/api2.png?raw=true)

* Response olarak dönen .png dosyasını API'a geri gönderdiğimizde ise sonuç,

![POSTMAN 2](https://github.com/kemalsanli/YMGK2-DJANGO-API/blob/main/api1.png?raw=true)

* Opsiyonel olarak yazdığımız arayüz,

![Arayüz 1](https://github.com/kemalsanli/YMGK2-DJANGO-API/blob/main/aray%C3%BCz%202.png?raw=true)

![Arayüz 2](https://github.com/kemalsanli/YMGK2-DJANGO-API/blob/main/aray%C3%BCz%203.png?raw=true)



## Ekip

Projeyi oluşturan ekip.

 Fatih ULUDAĞ  
 [@fatih-uludag](https://github.com/fatih-uludag)

 Kemal SANLI  
 [@kemalsanli](https://github.com/kemalsanli)


## Sürüm Geçmişi

* 1.0
    * Yayınlandı.

## Katılım
Pull Requestlere her zaman açığız.

## Teşekkürler
[opencv](https://github.com/opencv/opencv)

## Lisans
[MIT](https://github.com/kemalsanli/YMGK2-DJANGO-API/blob/main/LICENSE)
