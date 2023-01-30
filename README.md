# Mundial 2022 Qatar
Modele predykcyjne 

#### Dane do predykcji pochodzą z Kaggle(https://www.kaggle.com/datasets/brenda89/fifa-world-cup-2022) i są to rekordy meczów reprezentacji narodowych w latach 1993-2022 w oparciu o szereg zmiennych. W projekcie skupiłem się na tych reprezentujących oceny poszczególnych części drużyn(bramkarz,obrona,atak,środek pola) w oparciu o oceny z gry EA SPORTS FIFA oraz pozycje w rankingu FIFA. Ocena każdego z obszarów drużyny to średnia ocen zawodników - defensywa jest średnią ocen obrońców, atak - napastników itd. Dodatkowo, ze zbioru danych usunięte zostały obserwacje pochodzące z meczów towarzyskich oraz tych, w których nie brały udziału drużyny grające na mundialu. 

#### Do predykcji zbudowano model regresji logistycznej oraz sieci neuronowej, przy czym same predykcje wykonane zostały na modelu sieci, gdyż okazał się on stabilniejszy. Ta została zbudowana funkcją MLPClassifier() z pakietu sklearn. Model klasyfikuje 1 i 0, przy czym 1 to wygranie meczu przez pierwszą podaną drużynę, a 0 to jej przegrana, bądź remis.

#### Predykcje wykonywane są dwustronnie, co oznacza, że prawdopodobieństwo wygrania meczu jest liczone dla obu drużyn, a wygrywa ta, dla której jest ono wyższe. W przypadku, gdy predykcje dla obu rywalizujących drużyn wskazują na 0, werdyktem jest remis.
