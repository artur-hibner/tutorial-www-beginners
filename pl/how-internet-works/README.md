# Jak działa Internet?

> #### Info::Fragmenty tej sekcji została zaczerpnięte z tutoriala warsztatów Django Girls
>
> Bardzo dziękujemy twórcom [tutoriala Django Girls](http://tutorial.djangogirls.org/pl/) za udostępnienie nam tekstu rozdziału!

Możemy się założyć, że używacie go każdego dnia. Ale czy naprawdę wiecie co się dzieje, gdy wpisujecie w przeglądarce adres http://theawwwesomes.org i wciskacie <kbd>Enter</kbd>?

Aby zrozumieć jak działa Internet, powinniście najpierw dowiedzieć się czym tak naprawdę jest strona internetowa, a jest ona tylko zbiorem plików zapisanych na dysku twardym. Tak samo jak Wasze zdjęcia, muzyka czy filmy. Aczkolwiek strony internetowe różnią się od nich tym, że zawierają kod komputerowy zwany HTML.

Jeśli nie mieliście wcześniej do czynienia z programowaniem, może być Wam na początku trudno zrozumieć HTML, ale przeglądarki internetowe (takie jak Chrome, Safari, Firefox itd.) uwielbiają go. Zostały one zaprojektowane po to, by czytać ten kod, przetwarzać go i postępować zgodnie z jego instrukcjami. Prezentują pliki, z których składa się Wasza strona – by wyglądała dokładnie tak jak chcecie.

Tak jak w przypadku każdego innego pliku, musimy umiejscowić pliki HTML na dysku twardym. Do przechowywania plików HTML używamy specjalnych, potężnych komputerów zwanych <i>serwerami</i> (ang. <i>servers</i>). Serwery nie posiadają monitorów, myszy ani klawiatur, ich głównym celem jest przechowywanie danych i serwowanie ich. Dlatego są one nazywane <i>serwerami</i> – ponieważ służą do *serwowania* danych.

Ok, ale pewnie chcielibyście wiedzieć jak wygląda Internet?

Narysowaliśmy Ci schemat Internetu! Wygląda tak:

![Rysunek 1.1][1]

 [1]: /images/img1-2.png

Wygląda dość chaotycznie, prawda? W rzeczywistości jest to sieć połączonych między sobą maszyn (wspomnianych wyżej <i>serwerów</i>). Setki tysięcy maszyn! Wiele, wiele kilometrów kabli na całym świecie! Możecie wejść na stronę [Submarine Cable Map](http://submarinecablemap.com) i sami zobaczyć jak skomplikowana jest ta sieć. Oto zrzut ekranu ze strony internetowej:

![Submarine Cable Map][2]

 [2]: /images/submarine-map.png

To fascynujące, prawda? Ale oczywiście niemożliwe jest stworzenie bezpośredniego połączenia kablowego między każdym komputerem w Internecie. Więc aby dostać się do maszyny dostępnej w Internecie (na przykład tej, na której zapisane jest http://theawwwesomes.org), potrzebujemy wykonać zapytanie przechodzące przez wiele, wiele różnych maszyn.

Wygląda to tak:

![Rysunek 1.3][3]

 [3]: /images/img1-3.png

Wyobraźcie sobie, że po wpisaniu http://theawwwesomes.org, wysyłacie list o treści: "Drodzy Awwwesomes, chcę zobaczyć stronę <b>theawwwesomes.org</b>. Wyślijcie ją do mnie, proszę!"

List trafia do urzędu pocztowego najbliżej Was. Potem idzie do drugiego urzędu, który znajduje się trochę bliżej Waszego adresata. Potem do kolejnego, kolejnego, kolejnego, aż w końcu zostanie doręczony do miejsca przeznaczenia. Ciekawa rzecz: jeśli wyślecie wiele listów (<i>pakietów danych</i>) do tego samego adresata, mogą przejść przez zupełnie inne urzędy pocztowe (<i>routery</i>). To zależy od tego w jaki sposób zostaną rozdzielone w każdym urzędzie.

![Wysyłamy list][4]

 [4]: /images/img1-4.png

Tak, to takie proste. Wysyłacie wiadomości i oczekujecie jakiejś odpowiedzi. Oczywiście, zamiast papieru i długopisu używacie bitów danych, ale koncepcja jest dokładnie taka sama!

Zamiast adresów z nazwą ulicy, miastem, kodem pocztowym oraz nazwą kraju, używa się adresów IP. Wasze komputery najpierw pytają serwer DNS (system nazw domenowych, ang. DNS &ndash; Domain Name System) o przetłumaczenie theawwwesomes.org na adres IP. Działa to podobnie do dawnych książek telefonicznych, w których mogliście poszukać adresu czy numeru po nazwisku osoby, z którą chcieliście się skontaktować.

Listy muszą spełniać konkretne warunki, żeby zostały poprawnie doręczone: muszą posiadać adres, znaczek itd. Muszą być też napisane językiem zrozumiałym dla odbiorcy. To samo dotyczy <i>pakietów danych</i>, które wysyłacie, by zobaczyć jakąś stronę. Używany jest protokół HTTP (Hypertext Transfer Protocol).

Tak więc, ogólnie rzecz ujmując, jeśli chcecie mieć swoją stronę internetową musicie mieć <i>serwer</i> (komputer), gdzie będzie ona funkcjonować. Gdy <i>serwer</i> odbiera przychodzące <i>żądania</i> (Wasz list), wysyła Wam w odpowiedzi Waszą stronę (kolejny list).

## Co to jest programowanie frontend oraz backend?

Zapewne spotkaliście się już z terminami <i>frontend</i> i <i>backend</i>. Nazwy wskazują, że mogą dotyczyć one czegoś co znajduje się odpowiednio "z przodu" lub "z tyłu".

Przed chwilą wspomnieliśmy również o tym, że strona internetowa to nic innego, jak zbiór plików, które są przesyłane na nasz komputer z serwera znajdującego się gdzieś daleko. Fachowo mówi się wtedy, że nasz komputer jest <i>klientem</i>.

Programowanie frontend dotyczy zatem części klienckiej aplikacji. Jest to tworzenie kodu, który będzie wykonywany w Waszych przeglądarkach internetowych. Wszystko to, co "z przodu" powinno ładnie wyglądać, dlatego <i>frontendowiec</i> powinien wiedzieć, jak zakodować stronę, aby miała oczekiwany wygląd. Dane przesłane z serwera wymagają też czasem dodatkowego przetworzenia, oprócz tego należy obsłużyć wszelkie interakcje użytkownika ze stroną. To wszystko leży w zakresie obowiązków <i>frontend developera</i>.

Część backendowa jest natomiast "mózgiem" naszej strony. Programista backend jest między innymi odpowiedzialny za oprogramowanie pobierania i zapisywania danych z bazy. Ta część jest zupełnie niewidoczna, ale kluczowa dla działania każdej aplikacji webowej. Dobrym przykładem jest sklep internetowy. Wszystkie informacje o produktach dostępnych w sklepie znajdują się w bazie danych. Użytkownik chce mieć możliwość wyświetlania ich oraz filtrowania, aby znaleźć w sklepie swój wymarzony produkt. Cała logika związana z pobieraniem danych o produktach oraz ich filtrowaniem i przesyłaniem do przeglądarki użytkownika znajduje się po stronie backendu. Frontend odpowiada głównie za prezentację wyników po stronie użytkownika. <i>Et voilà!</i>
