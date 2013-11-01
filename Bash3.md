1\. Wyświetl plik /etc/passwd z podziałem na strony przyjmując, że strona na 5 linii tekstu. (raczej more niż less).
```
cat /etc/passwd | more -5-p-d

```
2\. Korzystając z polecenia cat utwórz plik tekst3.txt, który będzie składał się z zawartości pliku tekst1.txt,
ciągu znaków podanego ze standardowego wejścia (klawiatury) i pliku tekst2.txt.
```
cat >tekst3
cat tekst1 tekst2 >>tekst3

```
3\.Wyświetl po 5 pierwszych linii wszystkich plików w swoim katalogu domowym w taki sposób,
aby nie były wyświetlane ich nazwy.
```
head -n5 (sciezka) -q

```
4\.Wyświetl linie o numerach 3, 4 i 5 z pliku /etc/passwd.
```
head etc/passwd

```
