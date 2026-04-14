# 🧹 smartUserDataCleaner
Python ile hatalı ham verileri temizleme projesi.

## 1. Giriş
Bu projede girilen verilerin yanlış veya bozuk yazılma ihtimallerine karşın string fonksiyonlarını kullanarak düzeltilip aynı forma getirilmesi amaçlanmıştır. Veri temizleme, hatalı girdilerin bilgi kirliliği yaratmasını önlediği ve veri tutarlılığını sağladığı için yazılım sürecinde kritik bir öneme sahiptir. String işlemleri ise veri ön işleme aşamasında metinleri standardize ederek ham veriyi anlamlı ve işlenebilir hale getirmemizi sağlar. Bu yöntemle, düzensiz veriler ayıklanarak yazılımın daha güvenilir ve doğru sonuçlar üretmesi hedeflenir.

## 2. Kullanılan Python Konuları
* **Değişkenler:** Aldığımız verileri ve yaptığımız düzenlemeleri bir yerde tutmak ve kullanabilmek için değişkenler kullanıldı.
* **String veri tipi:** Metin yazılarının tutulduğu veri tipidir. Girdiden alınan veriler string olduğundan ötürü bu veri tipi kullanıldı.
* **String slicing:** Slicing işlemi mail kısmında mail kodu oluştururken otomatik olarak belli bir kısım alırken kullanıldı.
* **String metodları:**
    * `strip()`: Baştaki ve sondaki boşlukları temizler.
    * `lower()`: Metindeki tüm harfleri küçük harfe çevirir.
    * `title()`: Metindeki tüm kelimelerin baş harfini büyük, geri kalanını küçük harfe çevirir.
    * `split()`: Eğer fonksiyonda parantez içi boşsa kelimeleri her bir boşluktan ayırır. Eğer parantez içine bir karakter yazılırsa o karaktere göre ayırır.
    * `find()`: Parantez içine yazdığımız karakter aradığımız metinde varsa o karakterin indeksini verir. Eğer yoksa -1 döndürür.
* **Int ve float dönüşümü:** Gelen veriler string olarak alındığı için sayılarla bir işlem yapmak istediğimizde eğer string içindeki veride int veya float veri tipine uygunsa dönüşüm yapılır.

## 3. Veri Temizleme Süreci
Alınan ham veride fazla boşluklar, büyük-küçük harf yazımında hata, ve yapılması gereken birim dönüşümleri tespit edildi. Yanlış alınan veriler kodlarda ve çıktıda hataya ayrıca ekstra maliyete yol açabileceğinden veri temizleme süreci kritik öneme sahiptir.

* **1. Adım:** Alınan veriler kategorilerine göre ayrıldı ve fazla boşlukların yarattığı hata `strip()` ile giderildi. 
* **2. Adım:** İsim-soyisim için `split()` ile ayrıldı, küçük harfe çevrildi ve doğru yazım haline getirildi.
* **3. Adım:** Yaş hesabı için `float` tipine çevrildi ve istenen yaş yani 10 yıl sonraki yaş hesaplandı.
* **4. Adım:** Boy hesabı için `float` tipine çevrildi ve cm birimine çevrildi.
* **5. Adım:** Mail küçük harfe çevrildi, mailde zorunlu bulunan simge kontrol edildi ve ilk 3 karakterden alınan kod üretildi.

## 4. Sonuç ve Değerlendirme
Bu proje ile alınan ham ve bozuk veriler kategorilere ayrılarak düzeltildi ve standart hale getirildi. Gerçek hayatta da veri analizi ön işlemlerinde veya kullanıcı kayıt sistemlerinde otomatik olarak yapılan işlemler projede kullanıldı. String manipülasyonu, tip değişimi, slicing gibi beceriler kazanıldı.
