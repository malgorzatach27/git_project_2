## SPOSÓB DZIAŁANIA:


1. W pierwszej kolejności należy sklonować repozytorium z github do folderu o przykładowej ścieżce "C:\Users\Administrator\AppData\Roaming\QGIS\QGIS3\profiles\default\python\plugins" i pobrać do niego komendą "git pull" folder z zawartością wszystkich narzędzi do obsługi wtyczki
2. Uruchomić program Qgis, następnie wejść w zakładkę ''Wtyczki'' na pasku narzędzi, następnie z rozwijalnego paska wybrać opcję ''Zarządzanie wtyczkami''.
3. Na naszym ekranie powinno pojawić się okno, w którym po prawej stronie mamy zakładki do wyboru typu wtyczek, wybieramy: ''Zainstalowane'', gdzie powinny pojawić nam się wszystkie wtyczki zainstalowane w pamięci Qgis.
4. Wybieramy wtyczkę o nazwie ''plugin 12-14'', zaznaczamy ją ptaszkiem i automatycznie powinna nam się pojawić na pasku narzędzi z prawej strony.
5. Następnie możemy skorzystać z naszego pluginu klikając w jej ikonę, co spowoduje pojawienia się okna ze wtyczką.



## FUNKCJONALNOŚĆ:

(należy pamiętać, że w celu skorzystania ze wtyczki musimy mieć w bieżącym projekcie Qgis aktywną warstwę zawierającą pewną liczbę punktów) 



1. Obliczanie różnicy wysokości. 

Funkcja ta pozwala nam  obliczyć różnicę między wysokościami 2 punktów. <br>
	Aby z niej skorzystać należy: <br>
	- w rozwijalnym pasku wewnątrz wtyczki, po prawej stronie od nagłówka ''Select layer'' wybrać warstwę z której punkty chcemy analizować <br>
	- zaznaczyć 2 dowolne punkty na tej samej warstwie <br>
	- użyć przycisku "Calculate height difference" w oknie wtyczki <br>
	- obok przycisku pojawi nam się wartość różnicy wysokości między tymi punktami w metrach<br>

w przypadku zaznaczenia zbyt małej bądź zbyt dużej ilości puktów (innej niż 2), wtyczka nie wykona obliczeń, a zamiast tego zwróci nam stosowny komunikat o niepoprawnej ilości wybranych punktów.<br>



2. Obliczanie pól powierzchni.

Funkcja umożliwia nam obliczenie pola powierzchni poligonu utworzonego z dowolnej liczby punktów, jednak nie mniej niż 3.<br>
	Aby z niej skorzystać należy:<br>
	-w rozwijalnym pasku wewnątrz wtyczki, po prawej stronie od nagłówka ''Select layer'' wybrać warstwę z której punkty chcemy analizować<br>
	-wybrać co najmniej 3 dowolne punkty na tej samej, aktywnej warstwie<br>
   	-nasza wtyczka obsługuje wybór jednostki w której chcemy wyświetlić wynik<br>
		-aby uzyskać wynik w wybranej jednostce należy po prawej stronie od nagłówka "Select units" zaznaczyć kółko z jednym ze skrótów odpowiadającym konkretnym jednostkom [ha - hektar , m2 - metry kwadratowe, a - ary]<br>
	-użyć przycisku "Calculate surface area" w oknie wtyczki<br>
	-obok przycisku pojawi się nam wartość pola powierzchni poligonu utworzonego z wybranych punktów, w wybranej wcześniej jednostce<br>

w przypadku zaznaczenia zbyt małej ilości punktów (mniejszej niż 3), wtyczka zamiast wykonać obliczenia zwróci nam należyty komunikat o konieczności wyboru przynajmniej 3 punktów.



3. Rysowanie poligonów 

Funkcja umożliwia nam zobrazowanie poligonu, utworzonego poprzez wybrane wcześniej punkty do obliczenia wartości pola.<br>
	Aby z niej skorzystać należy:<br>
	-w rozwijalnym pasku wewnątrz wtyczki, po prawej stronie od nagłówka ''Select layer'' wybrać warstwę zawierającą punkty z których chcemy utworzyć poligon<br>
	-wybrać co najmniej 3 dowolne punkty na tej samej, aktywnej warstwie, zostaną one potraktowane jako wierzchołki powstałego poligonu<br>
	-w oknie wtyczki po prawej stronie użyć przycisku "Draw a polygon"<br>
	-zostanie wówczas wygenerowana nowa warstwa z powstałym graficznym przedstawieniem poligonu<br>
	


4. Wczytywanie danych numerycznych z plików tekstowych

Funkcja umożliwia nam wczytanie danych (koordynatów x,y) zawartych w plikach tekstowych o formacie .txt / .csv i wyświetlenie ich w tabeli na ekranie naszej wtyczki.<br>
	Aby z niej skorzystać należy:<br>
	-przygotować odpowiedni plik tekstowy w formacie (".txt" lub ".csv")<br>
	-wewnątrz wtyczki po prawej stronie od nagłówka "Select data file" wyświetla się puste pole oraz przycisk [...] z którgo należy skorzystać<br>
	-naciśniecie przycisku przekieruje nas do okna w którym musimy wybrać przygotowany wcześniej plik tekstowy<br>
	-w kolejnym kroku należy skorzystać z przycisku "Show coordinates preview" znajdującego się na ekranie wtyczki<br>
	-dane zawarte w pliku zostaną wyświetlone w postaci tabelarycznej w białym oknie znajdującym się w dolnej części interfejsu naszej wtyczki<br>
	


5. Czyszczenie bieżącego progamu na życzenie użytkownika.

Funkcja umożliwia użytkownikowi na żądanie czyszczenie konsoli wynikowej, wczytanych danych z plików tesktowych do okna wtyczki oraz zaznaczenia obiektów.<br>
-aby z niej skorzystać należy w dowolnym momencie użyć przycisku "Clear console and selection" <br>
-spowoduje to wyczyszczenie wymienionych powyżej parametryów podczas korzystania z wtyczki <br>
	-w przypadku korzystania z funkcji z podpunktu 3 (Rysowanie poligonów) pierwsze użycie przycisku do czyszczenia usuwa z projektu Qgis warstwę poligon utworzoną przy wykorzystaniu wtyczki<br>
	 natomiast drugie jego użycie usuwa widoczność polignu dla użytkownika i zaznaczenie punktów -->
