Najprostsza klatka animacji. Jak wygląda?
Wy przesyłacie opis takiej klatki do przeglądarki za pomocą CSS i HTML (chcę kwatrat w kolorze takim ...). 
Przeglądarka musi to wyświetlić. 
Zaczyna artysta. Tworzy szkic. Wygląda to tak, że blink 
1. przelicza style (jakie dokładnie parametry będzie miał element) - (recalculate style)
2. odświeża drzewo "warstw renderowania" (render layers); na razie możecie o tych warstwach jak o zbiorach elementów, które mają dokładnie taki sam z-index (nawet jeśli go nie podacie);
3. wykonuje szkic "paint" czyli zamienia dany element na jego reprezentacją w postaci komend, które mozecie znać jeśli na przykład robiliście coś na canvasie.
4. szkic zostaje przesłany do działu z pięknymi paniami, które go kolorują. Nie jest to trudna praca ale dość czasochłonna. Chrome korzysta tu z biblioteki SKIA - open source wykorzystywany np. przez Sublime Text


Co może utrudnić pracę artyście?
- głównie ilość elementów
- ale też ich skomplikowanie (np. box-shadow)
Dlaczego musimy na niego uważać i pilnować, żeby działał jak najszybciej?
....
Najporściej: blokuje innych. Nie tylko piękne panie. Pracuje w "main thread" a tam mamy do dyspozycji tylko 16ms

Co utrudnia pracę paniom?
- bardziej skomplikowanie styli niż ich ilość. np. "duuuży box-shadow"


zmienić left i top na 513; Dlaczego tylko jedna pani? I dlaczego pracuje szybciej?
...
odpowiedź znajduje się w zakładce "rendering".
W przeciwieństwie do tradycyjnej animacji gdzie każda pani dostaje całą klatkę tu potrzebujemy jak najszybciej jednej klatki.
Przeglądarki dzielą każdą warstwę (jedną "kartkę" celuloidu) na płytki (tiles) i każda pani dostaje jedną część. 
Liczbę pań mamy ograniczoną a dzięki podziałowi na płytki możemy wcześniej zacząć cokolwiek wyświetlać na ekranie.  
Możecie sobie wyobrazić, że te cztery panie dzielą warstwę celuloidu na 4 części, siedzą na około i malują wszystkie na raz.
Trwa to dłużej ale dzięki temu przeglądarka nie musi renderować całej strony (oszczędność pamięci) oraz podejrzewam,
że dla dużych elementów przy podziale na płytki można już zyskać na czasie.


Tiles 512x512 a 256 na retinie. Czy ma sens optymalizacja? Inne sposoby na optymalizację później.