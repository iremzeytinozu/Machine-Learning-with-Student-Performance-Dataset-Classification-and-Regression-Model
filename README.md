# Machine-Learning-with-Student-Performance-Dataset-Classification-and-Regression-Model

# Projenin Webinar Linki:
https://www.youtube.com/live/bBId8ttvRBQ?si=n6_jef3ycqk6c_Wm

# Projenin Amacı: 
Bu proje, öğrencilerin sınav başarılarını analiz etmek için bir dataset kullanır. Veri setinde öğrencilerin matematik, okuma ve yazma sınavlarında aldıkları puanlar ile çeşitli demografik ve sosyoekonomik faktörler bulunmaktadır. Bu proje, öğrenci başarısını etkileyen faktörleri inceler.

# Veri Seti
Kullanılan dataset, 1000 satırdan oluşmaktadır. Sütun isimleri ise sırasıyla şu şekilde: 
 * **gender:** Bu sütun cinsiyetleri göstermektedir
 * **race/ethnicity:** Bu sütun etnik kökene göre gruplandırmayı göstermektedir.
 * **parental level of education:** Bu sütun ebeveynlerinin eğitim seviyesini göstermektedir.
 * **lunch**: Bu sütun nasıl bir öğle yemeği türüne sahip olup olmadığını belirtir
 * **test preparation course:** Bu sütun test hazırlık kursuna katılıp katılmadığını göstermektedir.
 * **math score:** Bu sütun matematiksel notu göstermektedir.
 * **reading score:** Bu sütun okuma notunu göstermektedir.
 * **writing score:** Bu sütun yazma notunu göstermektedir.

# Değişkenler
Bağımlı değişken(y) **"math score"** sütunu, bağımsız değişkenler(x) ise **"math score"** sütunu hariç tüm satırlar olarak belirlenmiştir. Çeşitli regresyon algoritmaları denenerek bağımlı değişkeni bulmaya çalışılır. Bu projede kullanılan regresyon algoritmaları:

```python
from sklearn.linear_model import LinearRegression, Ridge, Lasso, ElasticNet, BayesianRidge
from sklearn.neighbors import KNeighborsRegressor
from sklearn.tree import DecisionTreeRegressor
from sklearn.ensemble import RandomForestRegressor, GradientBoostingRegressor
from sklearn.svm import SVR
from xgboost import XGBRegressor
from sklearn.model_selection import cross_validate
from sklearn.metrics import r2_score
```

# Model Seçimi 
En iyi performansı veren algoritma seçilir, hiperparametre optimize edilir ve seçilen algoritmanın değerlendirilmesi yapılır. Bu projede en iyi performansı veren regresyon modelinin **Ridge** olduğuna karar verilmiştir. Değerlendirme sürecinde bu projede **Ortalama Karesel Hata(Mean Squared Error), Ortalama Mutlak Hata(Mean Absolute Error)** kullanılmıştır.
