https://www.getresponse.com/resources/courses/landing-page-optimization-course.html

1. Skąd się biorą tak długie warstwy? (usunąć text-indent z '.rHeader .page-logo a')
2. Przyczyna dolnej długiej warstwy jest zaciemniony przez "squashing" (po kolei usunąć 'form-group' potem text-indent z 'body .footer .envelope')
3. Podejrzanie dużo warstw na spodzie. Zazwyczaj jest tylko jedna.
4. Google search - wyjaśnić dlaczego powoduje stworzenie dodatkowych warstw; zmienić z-index:-1 na visibility:hidden
5. Bardzo dużo warstw z przyczynami: 'overlapping', 'squashing'
6. Ustawić widok bokiem
7. Zmienić '.top' z-index na 1;
8. Czy można pozbyć się warstwy po lupą. Poza tym może zmniejszyć lupę.
9. odpalić fps meter