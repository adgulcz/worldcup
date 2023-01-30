# Mundial 2022 Qatar
## Modele predykcyjne 

#### Dane do predykcji pochodzą z Kaggle(https://www.kaggle.com/datasets/brenda89/fifa-world-cup-2022) i są to rekordy meczów reprezentacji narodowych w latach 1993-2022 w oparciu o szereg zmiennych. Zmienne to średnie oceny formacji drużyny zebrane z gry EA SPORTS FIFA(goalkeeper score, defense score, offense score, midfield score), ranking FIFA drużyny, kadencja trenera drużyny oraz średnia wartość zawodnika drużyny(te dwie ostatnie zostały dodane w modelu dla fazy pucharowej). Dodatkowo, ze zbioru danych usunięte zostały obserwacje pochodzące z meczów towarzyskich oraz tych, w których nie brały udziału drużyny grające na mundialu. 

#### Model dla fazy pucharowej został zbudowany na meczach z fazy grupowej (48 obserwacji). Uznałem, że żadne inne dane nie dopasują się lepiej do warunków obecnych mistrzostw świata niż te z niego pochodzące.

#### Do predykcji zbudowano model regresji logistycznej oraz sieci neuronowej, a do tego wykorzystany został pakiet sklearn. Modele klasyfikują 1 i 0, przy czym 1 to wygranie meczu przez pierwszą podaną drużynę, a 0 to jej przegrana, bądź remis.

#### Predykcje wykonywane są dwustronnie, co oznacza, że prawdopodobieństwo wygrania meczu jest liczone dla obu drużyn, a wygrywa ta, dla której jest ono wyższe. W przypadku, gdy predykcje dla obu rywalizujących drużyn wskazują na 0, werdyktem w fazie grupowej jest remis. W fazie pucharowej niedopuszczane są remisy, więc wartość prawdopodobieństwa wygrania meczu jest decydująca.
