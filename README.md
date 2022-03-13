# Bang-bang

Projektowanie układu sterowania typu: Bang-Bang w środowisku Stateflow/Simulink

Wnioski:

- Sterowanie typu bang-bang jest przełączaniem pomiędzy dwoma stanami. Za pomocą wzmocnienia sygnału sterującego można ustawić wybraną wartość histerezy.
- W obu zadaniach celem było uzyskanie jak najmniejszego przemieszczenia kulki. Parametry w regulatorze starałem dobierać się tak, żeby wartość procesowa oscylowała w granicach wartości zadanej, a histereza była jak najmniejsza. Optymalne parametry dobrałem metodą prób i błędów analizując przebiegi symulacji.
- Sterowanie jednocześnie uchybem i prędkością jest trudniejsze (ponieważ niewielkie zmiany prędkości dają duże zmiany przemieszczenia), ale daje lepsze efekty niż sterowanie samym uchybem. 
- W pierwszym zadaniu wartość zadaną ustawiłem na 0. Wykres uchybu e waha się od -0.01 do 0.01 m, a prędkości v od -0.0015 do 0.0015 m/s. Przemieszczenie x waha się w granicach od      -1.5*10^-6 do 1.5*10^-6 m. Myślę, że  jest to bardzo niewielkie przemieszczenie i zadanie zostało dobrze wykonane. Częstotliwość przemieszczenia jest bardzo duża, ponieważ w symulacji trwającej tylko 0.1 s widać, że okres drgań jest bardzo mały i wynosi 1.4 ms. Okres sygnału sterującego jest jeszcze mniejszy – wynosi ok. 20 μs.
- W zadaniu drugim obrót o bardzo mały kąt znacząco wpływa na przemieszczenie. Najlepsze warunki uzyskałem przy obrocie serwa o kąt pi/64. Dalsze zmniejszanie kąta nie wpływało na wartość procesową, więc nie było konieczne. Natomiast większe kąty nie zapewniały satysfakcjonującego przemieszczenia. Wartość zadaną ustawiłem na 0.005m i w takich granicach mieści się przemieszczenie. Uważam, że jest ono niewielkie w stosunku do całej długości bieżni, która wynosi 1 m. Przemieszczenie r jest zależne od sygnału sterującego theta, którego okres zwiększa się wraz z osiągnięciem przez przemieszczenie wartości zadanej. Uchyb e oscyluje wokół 0, a prędkość v od -0.003 do 0.003 m/s. Na początku, podczas narastania sygnału, wartość prędkości zmienia się tylko w zakresie wartości dodatnich. Po wystąpieniu histerezy jej amplituda zwiększa się.


