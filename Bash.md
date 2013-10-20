### Laboratorium 1

1\. Używając linii poleceń stwórz strukturę katalogów:

```sh
mkdir -p temp/ dom nauka/{c,logo,pascal,test}, praca/{dokumenty,zlecenia/{zrealizowane,niezrealizowane}}
```

2\. Przejdź do katalogu dom i utwórz katalog wazne-sprawy.
```sh
cd temp/dom
mkdir wazne-sprawy

```
3\. Wejdź do katalogu wazne-sprawy i utwórz tam pusty plik rachunki.txt.
```
cd temp/dom/wazne-sprawy
cat >rachunki.txt
^C

```
4\. Będąc w katalogu wazne-sprawy skopiuj plik rachunki.txt do katalogu zrealizowane.
```
cd temp/dom/wazne-sprawy
cp rachunki.txt ~/temp/praca/zlecenia/zrealizowane

```
5\. Przejdź do katalogu zrealizowane i zmień nazwę pliku rachunki.txt na wykonano.txt.
```
cd temp/praca/zlecenia/zrealizowane
mv ./rachunki.txt wykonano.txt
```
6\. Utwórz plik wykonano.txt wielkości 11 bajtów, następnie podziel go pliki wielkości 5 bajtów. W ten sposób otrzymasz 3 pliki. (split)
```
cd temp/praca/zlecenia/zrealizowane
cat >wykonano.txt
12345678901
^C
split -b 5 wykonano.txt
```
7\. Będąc w katalogu logo skopiuj powyżej otrzymane 3 pliki do katalogu dokumenty.
```
cd temp/nauka/logo
cp ~/temp/praca/zlecenia/zrealizowane/xa* ~/temp/praca/dokumenty
```
8\. Będąc w katalogu dokumenty połącz skopiowane 3 pliki w plik odtworzono.txt, tak aby otrzymać plik o zawartości identycznej z wykonano.txt.
   Następnie plik odtworzono.txt skopiuj do katalogu wazne-sprawy.
```
cd temp/praca/dokumenty
cat xaa xab xac >odtworzono.txt
cp odtworzono.txt ~/temp/dom/wazne-sprawy
```
9\. Będąc w katalogu wazne-sprawy sprawdź, czy są jakieś różnice w zawartości plików wykonano.txt i odtworzono.txt.
```
cd temp/dom/wazne-sprawy
diff wykonano.txt odtworzono.txt
```
10\. Wyświetl kalendarz na październik 2009 r. (cal)
```
cal 10 2009

```
 - Wyświetl kalendarz na wrzesień, październik i listopad 2009 r. z miesiącami obok siebie (cal):
 - Wyświetl kalendarz na październik, listopad i grudzień 2009 r. w taki sposób:
 - I jeszcze raz na wrzesień i październik oraz na październik i listopad 2009 r z miesiącami obok siebie (cal, cut?):

```
cal 10 2009 -3

cal 11 2009 -3


```

11\. Jaki był dzień tygodnia 25 maja 1975 r. (cal i date)
```

```



