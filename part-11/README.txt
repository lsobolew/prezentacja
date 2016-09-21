Uruchomić .psd
włączyć layer borders i paint flashing

Trochę podstaw:
Przeglądarka tworzy z CCS i HTML najpierw CSSOM i DOM a z nich tworzy Render Tree.
Każdy z RenderObject należy do RenderLayer


Tworząc RenderLayer decydujecie o tym w jakiej kolejności elementy mają być "malowane". 
RenderObject staje się Warstwą kiedy:
- ma position absolute albo relative;
- posiada transformację
- ma opacity inne niż 1
- i kilka innych (https://www.chromium.org/developers/design-documents/gpu-accelerated-compositing-in-chrome)
Bardziej po ludzku: oko, skrzydło ptaka nie będzie RenderLayer a dopiero cały ptak.

RenderLayer możemy utożsamiać z warstwami w Photoshop.
Przeglądarki wiedzą, że mogą zoptymalizować prędkość działania strony poprzez odpowiednie "pocięcie templaty"

Kiedy się na to decudują?



Pytanie 1: Jak potniecie taką stronę jeśli możecie używać jedynie tagów IMG (nie macie żadnych dodatkowych informacji poz tym co w pliku)
Pytanie 2: Grafik mówi Wam, że przy scrollowaniu słońce ma być zafiksowane.
Pytanie 3: Ptaszek będzie latał.

