<<<<<<< HEAD
# play-store-apps-analysis
=======
# Google Play Store Apps Analysis
"**[Google Play Store Apps](https://www.kaggle.com/datasets/lava18/google-play-store-apps)**" veri setini kullanarak Google Play Store'daki uygulama verilerindeki uygulama kategorileri, kullanıcı puanları, yüklenme sayıları ve diğer çeşitli metrikler arasındaki ilişkileri analiz amaçlı geliştirilen projedir. Verilerin analiz edilmesi, ön işlemden geçirilmesi, temizlenmesi ve görselleştirilmesi adımlarını içermektedir.

Veri seti aşağıdaki sütunları içermektedir:

* **App**: Uygulamanın adı

* **Category**: Uygulamanın kategorisi (Örneğin GAME, COMMUNICATION gibi)

* **Rating**: Kullanıcıların verdiği ortalama puan

* **Reviews**: Uygulamaya yapılan yorum sayısı

* **Size**: Uygulamanın boyutu

* **Installs**: Uygulamanın indirilme sayısı

* **Type**: Uygulamanın ücretli veya ücretsiz olma durumu

* **Price**: Uygulamanın fiyatı

* **Content Rating**: Uygulamanın hangi gruba uygun olduğu

* **Genres**: Uygulamanın türü/türleri

* **Last Updated**: Uygulamanın son güncellenme tarihi

* **Current Ver**: Uygulamanın mevcut sürüm numarası

* **Android Ver**: Uygulama için gereken minimum Android sürümü

## Yapılan Analizler ve Adımlar
Projenin kaynak kodları GooglePlayStoreAnalysis.ipynb adlı Jupyter Notebook dosyasında bulunmaktadır. Ana adımlar şunlardır:

1. Veri Temizleme ve Ön İşleme
* Eksik Verilerin İncelenmesi: Eksik veya hatalı (NaN) veriler tespit edildi ve uygun stratejilerle (örneğin hatalı bir satırın silinmesi) veri seti temizlendi.

* Veri Tiplerinin Dönüştürülmesi:

* "Reviews", "Size", "Installs" ve "Price" gibi sayısal olması gereken sütunlardaki metin ifadeler ("M", "k", "+", ",", "$") temizlenerek bu sütunlar sayısal (integer/float) veri tiplerine dönüştürüldü.

* "Last Updated" sütunu tarihsel analizler yapabilmek için datetime nesnesine dönüştürüldü ve bu tarihten Gün, Ay, Yıl bilgileri ayrı sütunlar olarak eklendi.

* "Android Ver" sütunundaki metin ifadeler temizlenerek daha anlaşılabilir bir hale getirildi.

* Tekrarlanan Verilerin Kaldırılması: Veri setinde bazı tekrarlanan veriler tespit edildi ve veri setinden çıkarılarak verilerin duplicate olması engellendi.

2. Keşifsel Veri Analizi(EDA=Exploratory Data Analysis) ve Görselleştirme
* Sayısal Değişkenlerin Dağılımı: "Rating", "Reviews", "Size" gibi sayısal özelliklerin dağılımları yoğunluk grafikleri (KDE plot) ile görselleştirilerek incelendi.

* Kategorik Değişkenlerin Analizi:

* Type (Ücretli/Ücretsiz) ve Content Rating (İçerik Derecelendirmesi) gibi kategorik değişkenlerin dağılımı sütun grafikleri (count plot) ile gösterildi.

* Kategori Bazında Yükleme Sayıları:

* En çok yüklenen ilk 10 uygulama kategorisi belirlendi ve bir çubuk grafiği ile görselleştirildi. GAME, COMMUNICATION ve TOOLS kategorilerinin en popüler kategoriler olduğu görüldü.

* En Popüler Kategorilerdeki En İyi Uygulamalar:

* Yükleme sayısına göre en popüler 5 kategorideki (GAME, COMMUNICATION, TOOLS, PRODUCTIVITY, SOCIAL) en çok indirilen ilk 5 uygulama listelendi ve görselleştirildi.

## Kullanılan Kütüphaneler

* pandas

* numpy

* matplotlib & seaborn


## Eğer Projeyi Çalıştırmak İsterseniz

1. Bu repoyu bilgisayarınıza klonlayın.

2. Gerekli kütüphaneleri yükleyin:

    ```bash
    pip install pandas numpy matplotlib seaborn jupyter
    ```
3. GooglePlayStoreAnalysis.ipynb dosyasını bir Jupyter Notebook ortamında açın ve hücreleri sırasıyla çalıştırın.
>>>>>>> 1c7bb27 (Uploaded project files)
