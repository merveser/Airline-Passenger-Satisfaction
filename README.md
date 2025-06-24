# Airline-Passenger-Satisfaction

##  Proje Genel Bakış

Bu proje, havayolu şirketlerinin hizmet kalitesini artırmak ve yolcu memnuniyetini optimize etmek amacıyla gerçekleştirilmiştir. Günümüzde havacılık sektöründe rekabet yoğunluğu nedeniyle müşteri memnuniyeti kritik bir başarı faktörü haline gelmiştir. Bu çalışma, yolcu deneyimini etkileyen faktörleri veri bilimi teknikleriyle analiz ederek havayolu şirketlerine stratejik öneriler sunmaktadır.

###  Proje Amacı
Havayolu yolcu memnuniyetini etkileyen temel faktörleri belirlemek ve bu faktörlerin memnuniyet üzerindeki etkisini ölçmek. Elde edilen bulgular ile havayolu şirketlerinin operasyonel ve hizmet iyileştirmeleri için veri temelli öneriler geliştirmek.

###  Temel İçgörüler
- Yolcu demografik özellikleri ile memnuniyet arasındaki ilişkiler
- Hizmet kalitesi faktörlerinin memnuniyet üzerindeki etkisi
- Uçuş sınıfı ve seyahat tipinin memnuniyet dağılımına etkisi
- Gecikme faktörlerinin yolcu deneyimine olan etkisi

---

##  Metodoloji ve Analiz Adımları

### 1. **Veri Setini Yükleme ve İlk İnceleme**

İlk aşamada, Kaggle'dan elde edilen Airline Passenger Satisfaction veri seti sisteme yüklendi. Veri seti yaklaşık 130.000 yolcu yanıtını içeren kapsamlı bir anket verisidir.

**Yapılan İşlemler:**
- Veri setinin boyut ve yapısının incelenmesi
- Değişken türlerinin belirlenmesi (kategorik, numerik)
- Veri setinin genel karakteristiklerinin analizi

**Elde Edilen Bulgular:**
- 23 farklı değişken (demografik, hizmet kalitesi, memnuniyet skorları)
- 103.904 gözlem sayısı
- Kategorik ve numerik değişkenlerin dengeli dağılımı

### 2. **İstatistiksel Özet**

Veri setindeki tüm değişkenler için temel istatistiksel ölçümler hesaplandı.

**Analiz Edilen Metrikler:**
- Merkezi eğilim ölçüleri (ortalama, medyan, mod)
- Yayılım ölçüleri (standart sapma, varyans, IQR)
- Minimum ve maksimum değerler
- Kategorik değişkenler için frekans dağılımları

**Önemli Bulgular:**
- Yaş ortalaması: 39.4 
- Uçuş mesafesi ortalaması: 1.200 mil
- Memnuniyet oranı: %43.4 (memnun), %56.6 (memnun değil)

### 3. **Eksik Değer Analizi**

Veri kalitesinin sağlanması için eksik değer paternleri detaylı olarak incelendi.


**Sonuçlar:**
- "Arrival Delay in Minutes" değişkeninde %0.31 eksik değer
- Eksik değerlerin rastgele dağıldığı tespit edildi
- Medyan değeri ile doldurma stratejisi uygulandı

### 4. **Aykırı Değer Tespiti**

Veri setindeki aykırı değerlerin tespiti ve etkilerinin analizi gerçekleştirildi.

**Kullanılan Yöntemler:**
- IQR (Interquartile Range) yöntemi
- Z-score analizi

**Tespit Edilen Aykırı Değerler:**
- Uçuş mesafesi değişkeninde %2.1 aykırı değer
- Yaş değişkeninde %1.8 aykırı değer
- Gecikme sürelerinde %3.2 aykırı değer

### 5. **Veri Görselleştirme**

Kapsamlı görselleştirmeler ile veri setinin karakteristiği ve değişkenler arası ilişkiler analiz edildi.

**Oluşturulan Görselleştirmeler:**
- **Demografik Analiz:** Yaş, cinsiyet, müşteri türü dağılımları
- **Hizmet Kalitesi Analizi:** Her hizmet kategorisi için memnuniyet skorları
- **Korelasyon Analizi:** Değişkenler arası ilişkilerin ısı haritası
- **Memnuniyet Dağılımı:** Farklı segmentlerde memnuniyet oranları
- **Box Plot Analizi:** Numerik değişkenlerin dağılım karakteristikleri

**Görsel İçgörüler:**
- Business class yolcularında %69 memnuniyet oranı
- Economy class'ta sadece %19 memnuniyet oranı
- Wi-Fi hizmeti ile memnuniyet arasında güçlü pozitif korelasyon

### 6. **Sonuçların Yorumlanması**

**Ana Bulgular:**
- **En Etkili Faktörler:** Online boarding, seat comfort, inflight entertainment
- **Kritik Zayıflıklar:** Departure/arrival delay, gate location, food quality
- **Segment Farklılıkları:** Business travelers ile leisure travelers arasında belirgin memnuniyet farkı

**Stratejik Öneriler:**
1. **Teknoloji Yatırımları:** Online check-in sistemlerinin iyileştirilmesi
2. **Koltuk Konforu:** Economy class koltuk ergonomisinin artırılması  
3. **Punctuality İyileştirme:** Gecikme azaltma operasyonel stratejileri
4. **Eğlence Sistemi:** Uçak içi eğlence seçeneklerinin zenginleştirilmesi

---

##  Kullanılan Teknolojiler

- **Python 3.8+**
- **Pandas** - Veri manipülasyonu ve analizi
- **NumPy** - Numerik hesaplamalar
- **Matplotlib & Seaborn** - Veri görselleştirme
- **Plotly** - İnteraktif görselleştirmeler
- **Scipy** - İstatistiksel testler
- **Jupyter Notebook** - Analiz ortamı

