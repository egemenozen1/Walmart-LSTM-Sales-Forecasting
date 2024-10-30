 Weekly_Sales (train_df): İlk grafik Weekly_Sales dağılımını gösteriyor. Satış değerleri oldukça sağa çarpık ve yoğunluk genellikle düşük değerlere yoğunlaşmış durumda. Bu çarpıklık, satış verilerinde birkaç yüksek değerin (muhtemelen tatil veya özel indirim dönemlerinde) olduğunu gösteriyor. Bu tür çarpıklıklar model performansını etkileyebilir, bu yüzden dönüşüm veya aykırı değerlerin işlenmesi düşünülebilir.

WeeklySales_MA_4 (train_df): Haftalık satışların hareketli ortalamasına baktığımızda, değerlerin çoğunlukla düşük seviyelerde yoğunlaştığını görüyoruz. Bu, satış verilerinin kısa vadeli ortalamalarının stabil olduğunu ve belirli zirve noktalarının olmadığını gösteriyor.

WeeklySales_Lag_1 ve WeeklySales_Lag_2 (train_df): Gecikmeli satış verileri (örneğin bir hafta ve iki hafta önceki satışlar) de düşük değerlerde yoğunlaşıyor. Bu durum, önceki haftaların satışlarının mevcut haftayı etkileyen bir eğilim oluşturduğunu gösteriyor. Ancak yine de büyük sapmalar var, bu yüzden bu gecikmeli değerlerin belirli dönemlerdeki zirveleri (tatiller veya indirim dönemleri gibi) açıklayıp açıklamadığı incelenebilir.

Temperature (features_df): Sıcaklık değerleri daha normal bir dağılım sergiliyor. Veriler ortalama değerler etrafında yoğunlaşmış, ancak uç noktalarda düşük bir sayı mevcut. Bu sıcaklık değişimlerinin satışlar üzerindeki etkisini daha iyi analiz edebilmek için bu özelliği mevsimsel etkilerle ilişkilendirmek faydalı olabilir.

Fuel_Price (features_df): Yakıt fiyatlarında bazı zirve noktaları mevcut, ancak genel olarak nispeten simetrik bir dağılım gösteriyor. Yakıt fiyatlarının ekonomik koşullara bağlı olarak satışlar üzerinde dolaylı bir etkisi olabilir, bu yüzden modelde bu değişkeni kullanmak mantıklı olabilir.

CPI (features_df): Tüketici Fiyat Endeksi (CPI) daha geniş bir dağılım sergiliyor. Bu, ekonomik durumdaki dalgalanmaları yansıtıyor olabilir. Özellikle düşük ve yüksek CPI değerlerinin satışlar üzerinde nasıl bir etkisi olduğunu incelemek önemli olabilir.

Unemployment (features_df): İşsizlik oranı genelde daha düşük seviyelerde yoğunlaşmış, ancak geniş bir aralığa yayılıyor. İşsizlik oranındaki artış veya düşüşler satışlara etkide bulunabilir, bu yüzden bu veriyi modelde dikkate almak önemli olabilir.

FuelPrice_Change (features_df): Yakıt fiyatlarındaki değişim, daha dar bir aralıkta yoğunlaşmış ve bu veri daha stabil bir yapıya sahip görünüyor. Yine de belirli değişimlerin etkisi modelde incelenebilir.

CPI_Lag_1 ve Unemployment_Lag_1 (features_df): Tüketici Fiyat Endeksi ve İşsizlik oranı gecikmeli verileri de benzer bir dağılım sergiliyor. Bu gecikmeli ekonomik göstergelerin, haftalık satışlar üzerindeki dolaylı etkilerini gözlemlemek açısından önemli olabilir.

Bu analizler doğrultusunda modellemede yer alacak özelliklerin etkilerini daha iyi anlamak için gerekirse dönüşümler veya etkileşim terimleri ekleyebiliriz. Ayrıca, modelde dikkat edilmesi gereken aykırı değerlerin belirlenmesi, çarpık dağılımların dönüşümle düzenlenmesi gibi adımlar faydalı olacaktır.