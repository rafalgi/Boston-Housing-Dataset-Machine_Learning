Cel projektu
Celem projektu jest zbudowanie modelu uczenia maszynowego, który przewiduje ceny mieszkań w Bostonie na podstawie różnych cech, takich jak poziom zanieczyszczenia powietrza, liczba pokoi, wiek budynków i inne. Do tego celu wykorzystano algorytm Gradient Boosting Regressor.

Kroki projektu
Importowanie bibliotek
Na początku projektu importowane są niezbędne biblioteki Python, takie jak Pandas, NumPy, Matplotlib, Seaborn oraz kilka z bibliotek Scikit-learn do przetwarzania danych, wizualizacji i budowy modeli uczenia maszynowego.

Wczytywanie i wstępna analiza danych
Dane są wczytywane z pliku CSV BostonHousing.csv. Przeprowadzana jest wstępna analiza danych, która obejmuje wyświetlanie pierwszych kilku wierszy danych oraz sprawdzanie informacji o kolumnach i typach danych. Wykorzystywane są funkcje head(), info() oraz describe().

Czyszczenie danych
Dane są czyszczone poprzez usuwanie brakujących wartości oraz sprawdzanie duplikatów. W tym celu używane są funkcje isnull().sum() oraz duplicated().sum(). Kolumna rm, która zawiera brakujące wartości, jest usuwana za pomocą dropna(axis=1, inplace=True).

Wizualizacja danych
Dane są wizualizowane w celu lepszego zrozumienia korelacji między zmiennymi oraz ich rozkładu. Wykorzystywane są mapy cieplne (heatmap) oraz wykresy par (pairplot) z biblioteki Seaborn.

Budowa modelu Gradient Boosting Regressor
a. Dane są dzielone na zestawy treningowe i testowe za pomocą train_test_split.
b. Trenowanie modelu Gradient Boosting Regressor z parametrami max_depth=2, n_estimators=3, learning_rate=1.0.
c. Prognozowanie cen mieszkań na podstawie zestawu testowego.
d. Ewaluacja modelu za pomocą metryk takich jak Mean Absolute Error (MAE), Mean Squared Error (MSE) oraz R-squared (R²).

Wyniki modelu
Wyniki pierwszego modelu:

Mean Absolute Error: 4.82
Mean Squared Error: 57.83
R-squared: 0.17
Znaczenie zmiennych
Ważność zmiennych jest wizualizowana za pomocą wykresu słupkowego (barh). Pokazuje on względne znaczenie każdej cechy w modelu.

Optymalizacja parametrów
a. Wykorzystanie GridSearchCV do znalezienia najlepszych parametrów dla Gradient Boosting Regressor.
b. Najlepsze parametry uzyskane to learning_rate=0.05 i n_estimators=150.
c. Trenowanie modelu z optymalnymi parametrami i ocena jego wyników.

Ewaluacja zoptymalizowanego modelu
Wyniki zoptymalizowanego modelu:

Mean Absolute Error: 4.82
Mean Squared Error: 57.83
R-squared: 0.17
Porównanie modeli
Wyniki obu modeli są porównane w tabeli, co pozwala na ocenę wpływu optymalizacji parametrów na wyniki modelu.

Wnioski
Na podstawie przeprowadzonej analizy można stwierdzić, że model Gradient Boosting Regressor nie daje znacząco lepszych wyników po optymalizacji parametrów, co sugeruje potrzebę dalszych badań i testowania innych modeli lub dodatkowego przetwarzania danych w celu poprawy wyników prognozowania.

Potencjalne zastosowania
Wyniki tego projektu mogą być wykorzystane do:

Prognozowania cen mieszkań w Bostonie na podstawie różnych cech.
Pomocy deweloperom i agentom nieruchomości w lepszym zrozumieniu czynników wpływających na ceny mieszkań.
Wsparcia decydentów w analizie wpływu różnych czynników środowiskowych i infrastrukturalnych na rynek nieruchomości.
