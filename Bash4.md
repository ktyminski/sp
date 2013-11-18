Laboratorium 4
--
1\. Wyświetl listę plików z aktualnego katalogu, zamieniając wszystkie małe litery na duże
```
ls -1F | sed -e '/[/]/d' | tr 'a-z' 'A-Z'
```
2\. Wyświetl listę praw dostępu do plików w aktualnym katalogu, ich rozmiar i nazwę
```
ls -hgoF --full-time | tr -s " " | cut -f 1,3,7 -d " " | sed -e '/[/]/d' | tr " " "\t"
```
3\. Wyświetl listę plików w aktualnym katalogu, posortowaną według rozmiaru pliku
```
ls -1lS | sed -e '/^d/d' | tr -s " " | cut -f 5,9 -d " " | tac
```
4\. Wyświetl zawartość pliku /etc/passwd posortowaną według numerów UID w kolejności od największego do najmniejszego
```
cat /etc/passwd | sort -t : -k 3 -nr
```
5\. Wyświetl zawartość pliku /etc/passwd posortowaną najpierw według numerów GID w kolejności od największego do najmniejszego, a następnie UID
```
cat /etc/passwd | sort -t : -k 4 -nr -k 3 -nr
```
6\. Podaj liczbę plików każdego użytkownika
```
find -type f -printf "%U\n" | sort | uniq -c | sort
```
7\. Sporządź statystykę praw dostępu (dla każdego z praw dostępu podaj, ile razy zostało ono przydzielone)
```
find -type f -printf "%m\n" | sort | uniq -c
```
