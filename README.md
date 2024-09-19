# MLproject zeynep nergiz kanat
 zeynep nergiz kanat ml proje
# Human Activity Recognition Projesi

Bu proje, Human Activity Recognition veri seti üzerinde gözetimli ve gözetimsiz öğrenme algoritmalarını kullanarak aktivitelerin tanınmasını hedeflemektedir. Projenin amacı, iki farklı öğrenme türünü karşılaştırmak ve hangi algoritmanın bu veri seti için daha uygun olduğunu belirlemektir.

## Veri Seti

Veri seti, insan aktivitelerinin (yürüme, oturma, ayakta durma vb.) sınıflandırılmasını sağlamak amacıyla kullanılmıştır. Özellikler sensör verilerini temsil ederken, 'Activity' sütunu sınıflandırılacak etiketleri temsil eder.

## Kullanılan Algoritmalar

Projede iki farklı öğrenme türü kullanılmıştır:

### Gözetimli Öğrenme: RandomForestClassifier
- Random Forest algoritması ile insan aktiviteleri sınıflandırıldı.
- Veriler, `train_test_split` ile eğitim ve test setlerine ayrıldı, ardından `StandardScaler` ile ölçeklendirildi.

### Gözetimsiz Öğrenme: KMeans
- KMeans algoritması ile aynı veri seti üzerinde kümeleme yapıldı.
- Veri seti, 6 farklı kümeye ayrıldı ve bu kümeler aktiviteleri temsil etmeye çalıştı.
- KMeans sonuçları, görsel olarak grafiklerle sunuldu.

## Sonuçlar

- **Gözetimli Öğrenme (RandomForestClassifier)** modeli, veri seti sınıflandırmaya uygun olduğu için yüksek doğruluk oranı (%99) ile iyi sonuçlar verdi.
- **Gözetimsiz Öğrenme (KMeans)** algoritması, etiketler olmadan çalıştığı için sınıflandırmada daha düşük performans gösterdi. Bu, kümeleme algoritmasının veri setinin yapısına göre daha uygun olmayabileceğini gösteriyor.

## Seçilen Algoritma ve Veri Setinin Uyumu

- **RandomForestClassifier**, veri setinde etiketli bir sınıflandırma problemi olduğu için bu veri seti üzerinde oldukça başarılıdır. Bu algoritma, her bir aktivitenin hangi sınıfa ait olduğunu öğrenerek tahmin yapabilir.
- **KMeans** ise veri setinde etiket bulunmadığında kullanılır ve kümeler oluşturarak veriyi sınıflandırmaya çalışır. Ancak bu veri setinde etiketli veriler bulunduğundan dolayı KMeans'in sınıflandırma başarısı düşük olacaktır. Bu sebeple, bu veri seti gözetimli öğrenme algoritmaları için daha uygundur.

## Projeye Genel Bakış

Bu projede, hem gözetimli hem de gözetimsiz öğrenme algoritmalarının performansı karşılaştırılmıştır. **RandomForestClassifier**, etiketli veri ile çalıştığı için daha yüksek performans gösterirken, **KMeans** kümeleme algoritması, etiketlenmemiş veri ile çalıştığı için beklenenden daha düşük sonuçlar vermiştir.

## Kaggle Notebook Linki

Projeyi detaylı incelemek için Kaggle üzerindeki notebook'a [buradan](https://www.kaggle.com/code/zeynepnergizkanat/mlproject) ulaşabilirsiniz.
