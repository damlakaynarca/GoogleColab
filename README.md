# GoogleColab
5 katmandan oluşan bir CNN modeli ve adım  adım uygulanışı
Kod, TensorFlow kütüphanesini kullanarak el yazısı rakam tanıma (MNIST) veri seti üzerinde bir evrişimli sinir ağı (CNN) modeli oluşturmayı ve eğitmeyi amaçlar.  Kodun adım adım açıklaması:

1. **TensorFlow Kütüphanesinin İçeri Aktarılması**: İlk satırda TensorFlow kütüphanesi içe aktarılır.

2. **MNIST Veri Setinin Yüklenmesi**: `tf.keras.datasets.mnist` fonksiyonu kullanılarak MNIST veri seti yüklenir. Bu veri seti, el yazısı rakamların gri tonlamalı görüntülerini içerir.

3. **Verilerin Normalize Edilmesi**: Görüntü verileri (x_train ve x_test) 0 ile 1 arasında ölçeklenir, böylece daha hızlı eğitim yapılır.

4. **Modelin Oluşturulması**: `tf.keras.models.Sequential()` fonksiyonu kullanılarak bir sıralı model oluşturulur. Model, evrişimli sinir ağı (CNN) katmanlarından ve tam bağlantılı gizli katmanlardan oluşur.

5. **Modelin Derlenmesi**: `model.compile()` fonksiyonu, modelin eğitim sürecini yapılandırır. Kayıp fonksiyonu olarak "sparse_categorical_crossentropy" kullanılır.

6. **Modelin Eğitilmesi**: `model.fit()` fonksiyonu kullanılarak model eğitilir. Eğitim verisi (`x_train` ve `y_train`) kullanılarak model, belirli bir sayıda dönem (epoch) boyunca eğitilir.

7. **Modelin Değerlendirilmesi**: `model.evaluate()` fonksiyonu kullanılarak modelin test veri seti üzerindeki performansı değerlendirilir. Bu işlem, modelin kayıp (loss) ve doğruluk (accuracy) metriklerini hesaplar.

8. **Sonuçların Yazdırılması**: Test doğruluğu (`test_acc`) ekrana yazdırılır.

Bu kod, MNIST veri setindeki el yazısı rakamları tanımlamak için oldukça yaygın olarak kullanılan bir modelin uygulamasını içerir.
