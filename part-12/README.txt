Layer explosion
Warstwy tworzone z powodów bezpośrednich nie są dużym problemem. Zazwyczaj lepiej, że przeglądarka je tworzy niż gdyby tego nie robiła.
Problemem jest tzw. "layer explosion". Niektóre "render layers" stają się "graphics layers" tylko po to aby zachować spójność strony.

Dlaczego na tej stronie pojawia się tyle warstw? Gdy element otrzymuje animację to chrome tracin kontrolę nad jego chwilowym położeniu
i musi załozyć, że element może znaleźć się wszędzie.

Co to render layers?
DOM == Render Objects <= Render Layers <= Graphics Layers