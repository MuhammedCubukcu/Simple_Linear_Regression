# Basit Doğrusal Regresyon / Linear Regresyon

## Regresyon
Regresyon modelleri (hem doğrusal hem de doğrusal olmayan), örnegin maaş gibi gerçek bir değeri tahmin etmek için kullanılır. Bağımsız değişkeniniz zaman ise gelecekteki değerleri tahmin ediyorsunuzdur, aksi halde modeliniz mevcut ancak bilinmeyen değerleri tahmin ediyordur.
* Simple Linear Regression.
* Multiple Linear Regression
* Polynomial Regression
* Support Vector for Regression (SVR)
* Decision Tree Regression.
* Random Forest Regression.

## Simple Linear Regression:
Simple linear regresyon, 2 nicel veri arasındaki ilişkiyi özetleyen istatiksel bir metoddur. Bağımsız değişkenlerin (X) değerlerini temel alarak bağımlı değişkeni (Y) tahmin etmenin bir yöntemidir. İki değişkenin doğrusal olarak birbirleri ile ilişkili olduğu varsayılmaktadır.

Basit doğrusal regresyon bize normal dağılmış, belirli bir oranda  veri toplanmış iki değişken arasında doğrusal ilişki olup olmadığını test etme olanağı vermektedir.

Y bağımlı ve X bağımsız değişken olmak üzere, Y ile X değişkenleri arasındaki sebep- sonuç ilişkisini matematiksel model olarak ortaya koyan yönteme regresyon denir. Bu ilişkiyi doğrusal  bir şekilde ortaya koyan bir işlev bulmaya çalışırız. Formülde  basit bir doğrusal regresyon formülü verilmiştir.

### ŷ = b0 + b1.X₁

* ŷ = Dependent Variable
* b0 = y-intercept (constant)
* b1 = Slope coefficient
* X₁ = independent Variable

### Linear Regresyon;

* Hava durumu tahminlerinde
* Borsa Tahminlerinde
* Belirli bir bölgede ortalama ev fiyatlarını çıkarmada
* Bir ürüne olan talebi gösterme vb. alanlarda kullanılmaktadır.

## Adım 1 : Veri Ön işleme 

* Kütüphanelerin import edilmesi,
* Veri setinin yüklenmesi,
* Eksik değerlerin kontrolü,
* Veri Setinin test  ve train olarak bölünmesi,

## Adım 2 : Basit Doğrusal Regresyon Modelinin Uygulanması (Fit)

Veri seti ile modeli eğitmek  için sklearn.linear_model kütüphanesinden LinearRegression sınıfını kullanacağız. Sonra LinearRegression sınıfında  bir regressor  nesnesi oluşturuyoruz. Şimdi regressor nesnemizle birlikte Linear Regression sınıfının fit() metodunu kullanarak modelimizi eğitiyoruz.

```Python
from sklearn.linear_model import LinearRegression

regressor = LinearRegression()

regressor.fit(X_train, y_train)
```

## Adım 3 : Sonucu Tahmin Etmek 
Basit linear nesnemizi oluşturup modelimizi eğittikten sonra şimdi de gözlemlerimizi, ayırdığımız x_test verilerini kullanarak tahmin edeceğiz.  Daha önce oluşturduğumuz regressor nesnemizi  predict() metodu ile tekrar kullanıyoruz ve   çıktımızı y_pred vektörüne kaydediyoruz. Y_pred değerleri modelin bizim için tahmin ettiği değerlerdir.

```python
y_pred = regressor.predict(X_test)
```

## Adım 4 : Görselleştirme

Son aşamamız ise sonuçlarımızın görselleştirilmesidir, Eğitim seti sonuçlarımızın saçılma grafiklerini çizmek için matplotlib.pyplot kütüphanesini ve modelimizin değerleri ne kadar yakın tahmin ettiğini görmek için test sonuçlarını kullanacağız.

### Yapılan Çalışma Hakkında:
*  Yapılan uygulamada çalışanların tecrübelerine göre maaş tahmini yapan bir model geliştirme yapılmıştır.
*  Basit Doğrusal Regresyonu anlamak için temel bir veri seti ile çalışılmıştır.
* Kodu incelemek için main.py uzantılı dosya içerisine bakabilirsiniz.
# English

# Simple Linear Regression / Linear Regression

## Regression
Regression models (both linear and nonlinear) are used to predict a true value, such as salary. When you have independent variability, you estimate the values you set, otherwise your model is guessing at existing but unknown values.
* Simple Linear Regression.
* Multiple Linear Regression
* Polynomial Regression
* Support Vector (SVR) for Regression
* Decision Tree Regression.
* Random Forest Regression.

## Simple Linear Regression:
Simple linear regression is a statistical method that summarizes the concatenation between 2 nice data. It is a method of estimating the base variable (Y) based on the values of the independent variables (X), assuming that the two variables are linearly related.

Simple linear regression gives us the power to test whether there is a linear relationship between two variables that are normally distributed and data is collected from a certain point.

The method that puts the middle as a model that processes the cause-effect relationship between the variables Y and X, where Y is a locked variable and X is an independent variable, is called regression.

### ŷ = b0 + b1.X₁

* ŷ = Dependent Variable
* b0 = y-intercept (constant)
* b1 = Slope coefficient
* X₁ = independent Variable

### Linear Regression;

* In weather forecasts
* In Stock Market Predictions
* Inferring average house prices in a regional area
* Showing demand for a product, etc. It is used in areas.

## Step 1: Data Preprocessing

* Import of libraries,
* Software of the data set,
*Checking missing values,
* Complements of the Data Set as testing and training,

## Step 2: Applying the Simple Linear Regression Model (Fit)

We will use the LinearRegression class from the sklearn.linear_model library to train the model with the dataset. Then we create a regressor object in the LinearRegression class. Now we train our model using the fit() method of the Linear Regression class with our regressor object.

```Python
import LinearRegression from sklearn.linear_model

regressor = LinearRegression()

regressor.fit(X_train, y_train)
```

## Step 3: Predicting the Outcome
After creating our simple linear object and training our model, predictions are now made using our observations and the x_test parts we separated. We reprocess our previously created regressor object with the predict() method and save our output to the y_pred vector. Y_pred values are the values predicted for us in the model.

```python
y_pred = regressor.predict(X_test)
```

## Step 4: Visualization

Our final stage is visualizing our results, we will use the matplotlib.pyplot library to draw scatter plots of our training set results and we will test it to see how closely you can predict the values of our model.

### About the Study:
* In the application, a model was developed that predicts salaries according to the experiences of employees.
* A basic data set was used to understand Simple Linear Regression.
* To examine the code, you can look at the file with main.py extension.


