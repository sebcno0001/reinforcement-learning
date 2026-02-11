# Q-Learning z Gymnasium

Implementacja algorytmu Q-learning dla środowisk Gymnasium (OpenAI Gym) w ramach laboratorium ze sztucznej inteligencji.

## 📋 Opis projektu

Projekt zawiera implementacje algorytmu Q-learning dla dwóch różnych środowisk:

1. **Blackjack-v1** - Agent uczący się gry w Blackjacka
2. **MountainCar-v0** - Agent uczący się prowadzenia samochodu na wzgórze

## 🚀 Technologie

- Python 3.x
- Gymnasium (OpenAI Gym)
- NumPy
- Matplotlib

## 📦 Instalacja

```bash
pip install gymnasium numpy matplotlib
```

## 🎮 Środowiska

### Blackjack

Agent uczy się optymalnej strategii gry w Blackjacka:
- **Liczba epizodów treningu**: 500,000
- **Współczynnik uczenia (alpha)**: 0.1
- **Współczynnik dyskontujący (gamma)**: 0.99
- **Epsilon (eksploracja)**: 0.1

Wyniki testowe pokazują:
- Liczbę wygranych, przegranych i remisów
- Skuteczność agenta w %
- Wizualizację średniej ruchomej nagród

### MountainCar

Agent uczy się wypychania samochodu z doliny na wzgórze:
- **Liczba epizodów treningu**: 50,000
- **Dyskretyzacja stanu**: (18, 14) - pozycja i prędkość
- Problem ciągłego przestrzeni stanów rozwiązany przez dyskretyzację

## 📊 Wyniki

Notebook generuje:
- Wykresy uczenia (średnia ruchoma nagród)
- Statystyki wydajności agenta
- Wizualizacje wyników testowych (dla Blackjacka)

## 🎯 Użycie

Uruchom notebook `lab4_arisc.ipynb` i wykonaj kolejne komórki:
1. Pierwsza komórka - podstawowa wersja Blackjacka
2. Druga komórka - rozszerzona wersja z dodatkowymi wizualizacjami
3. Trzecia komórka - MountainCar

## 📈 Parametry Q-learning

| Parametr | Wartość | Opis |
|----------|---------|------|
| alpha (α) | 0.1 | Współczynnik uczenia |
| gamma (γ) | 0.99 | Współczynnik dyskontujący |
| epsilon (ε) | 0.1 | Współczynnik eksploracji |

## 🔍 Algorytm

Implementacja klasycznego Q-learningu:

```
Q(s,a) ← Q(s,a) + α[r + γ·max(Q(s',a')) - Q(s,a)]
```

Gdzie:
- `s` - aktualny stan
- `a` - wybrana akcja
- `r` - nagroda
- `s'` - następny stan
- `α` - współczynnik uczenia
- `γ` - współczynnik dyskontujący

## 📝 Uwagi

- Q-tabela reprezentowana jest jako `defaultdict` dla efektywnej pamięci
- Agent używa strategii ε-greedy (epsilon-greedy) do balansowania eksploracji i eksploatacji
- Dla MountainCar zastosowano dyskretyzację przestrzeni ciągłej

## 👤 Autor

Projekt laboratoryjny - Sztuczna inteligencja

## 📄 Licencja

MIT License
