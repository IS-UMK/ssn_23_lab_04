# SSN. Lab. 4. Generalizacja MLP

Zapoznaj się z zawartością notatnika Jupyter umieszczonego w repozytorium  i wykonaj zawarte w nim ćwiczenia.

Notatnik: [04_mlp_test.ipynb](https://github.com/IS-UMK/ssn_23_lab_04/blob/master/04_mlp_test.ipynb)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/IS-UMK/ssn_23_lab_04/blob/master/04_mlp_test.ipynb) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/IS-UMK/ssn_23_lab_04/master?filepath=04_mlp_test.ipynb)

---

## Zad. 4. Wykrywanie raka piersi (Wisconsin Diagnostic Breast Cancer)

Znajdź najlepszy model klasyfikacji MLP zrealizowany za pomocą klasy ``MLPClassifier`` wykrywający złośliwe przypadki raka piersi w danych `WDBC`. Dane można wczytać za pomocą funkcji [sklearn.datasets.load_breast_cancer()](https://scikit-learn.org/stable/modules/generated/sklearn.datasets.load_breast_cancer.html).


```python
from sklearn.datasets import load_breast_cancer
data = load_breast_cancer()
X = data['data']
y = data['target']
```

Dane zawierają wyniki badań 569 pacjentów z rakiem piersi. Każdy przypadek opisany jest 30 ciągłymi atrybutami. Dane podzielone są na dwie klasy: 0 to grupa nowotworów łagodnych (`malignat`), wartość 1 to nowotwory złośliwe (`benign`). 

1. Podziel zbiór na część treningową zawierającą piersze 400 przypadków oraz część testową zawierjącą pozostałe przypadki
2. Kożystając **wyłacznie ze zbioru treningowego** zbuduj model klasyfikacji MLP dobierając parametry sieci neuronowej.  Spróbuj wykorzystać do tego celu mechanizm strojenia parametrów poprzez przeszukiwanie siatką (`GridSearchCV`). Wykonaj strojenie parametrów dla przynajmniej 3 z podanych poniżej:
    * ilość warstw i ilość neuronów  w warstwach
    * stałą uczenia
    * typ funkcji aktywacji
    * współczynnik reglaryzacji L2
    * wspólczynnik momentu
    * wielkość paczki
3. Oceń skuteczność klasyfikacji uzyskanego modelu na **zbiorze testowym**. 

Rozwiązanie w postaci notatnika Jupyter (``.ipynb``) lub skrypt w języku Python (``.py``) umieść w Moodle lub prześlij do repozytorium GitHub.

