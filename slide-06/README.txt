Włączyć paint flashing.
Pokazać najpierw strukturę: trzy sekcje z czego jedna ma background-position:fixed;


Robienie background-position:fixed to tak jakby przypiąć tło do body i na każdym skrolu je przesuwać. 
Body jest wysokie a background zawsze na viewporcie a to powoduje repaint.

Wyłączyć background z section;
Pokazać ::before

Wniosek: Czysty CSS !== wydajność;

Position: fixed powoduje jednak powstanie dodatkowej warstwy co prowadzi do drugiej części.