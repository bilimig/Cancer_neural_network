**README**

## Przewidywanie Diagnozy Nowotworowej za Pomocą Sieci Neuronowych

### Przegląd
Implemetacja modelu sieci neuronowej do przewidywania diagnozy nowotworowej na podstawie cech wejściowych. Model jest trenowany przy użyciu zbioru danych `cancer.csv`, gdzie każdy wiersz reprezentuje pacjenta z różnymi cechami związanymi z diagnozą nowotworu.

### Architektura Modelu
Model sieci neuronowej używany w tym kodzie składa się z:
- Warstwy wejściowej z 30 cechami
- Dwóch warstw ukrytych, każda z 8 neuronami
- Warstwy wyjściowej z 2 neuronami (do klasyfikacji binarnej: złośliwy lub łagodny)

### Użyte Biblioteki
- `torch` i `torch.nn`: Do budowania i trenowania modeli sieci neuronowej.
- `pandas`: Do manipulacji i przetwarzania danych.
- `sklearn.model_selection`: Do podziału zestawu danych na zestawy treningowy i testowy.
- `matplotlib.pyplot`: Do wizualizacji postępów w treningu.

### Trening Modelu
- **Funkcja Straty**: CrossEntropyLoss
- **Optymalizator**: Optymalizator Adam z współczynnikiem uczenia 0.001
- **Epoki**: 5000

Podczas treningu monitorowane są strata i dokładność modelu w kolejnych epokach, aby ocenić jego wydajność.

### Analiza Wyników
Po treningu wydajność modelu jest oceniana na zbiorze testowym. Obliczana jest osiągnięta dokładność, a dokonywane są również pojedyncze predykcje na zbiorze testowym, aby ustalić, ile z nich było poprawnych.

### Dołączone Pliki
- `cancer.csv`: Zbiór danych zawierający informacje o pacjentach i etykietach diagnozy.
