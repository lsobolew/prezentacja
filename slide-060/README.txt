Uruchomić .psd

Pytanie 1: Jak potniecie taką stronę jeśli możecie używać jedynie tagów IMG (nie macie żadnych dodatkowych informacji poz tym co w pliku)
Pytanie 2: Grafik mówi Wam, że przy scrollowaniu słońce ma być zafiksowane.
Pytanie 3: Ptaszek będzie latał.

To samo robi przeglądarka:
Wy dostajecie warstwy; przeglądarka tworzy z CCS i HTML najpierw CSSOM i DOM a z nich tworzy Render Tree a każdy z RenderObject należy do RenderLayer
https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction?hl=en


Tworząc RenderLayer decydujecie o tym w jakiej kolejności elementy mają być "malowane". 
RenderObject staje się Warstwą kiedy:
- ma position absolute albo relative;
- posiada transformację
- ma opacity inne niż 1
(więcej na https://www.chromium.org/developers/design-documents/gpu-accelerated-compositing-in-chrome)

RenderLayer możemy utożsamiać z warstwami w Photoshop.
Przeglądarki wiedzą, że mogą zoptymalizować prędkość działania strony poprzez odpowiednie "pocięcie templaty"

Kiedy się na to decudują?


