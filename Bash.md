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
mv rachunki.txt ./temp/praca/zlecenia/zrealizowane

```
5\. Przejdź do katalogu zrealizowane i zmień nazwę pliku rachunki.txt na wykonano.txt.
```
cd temp/praca/zlecenia/zrealizowane
mv ./rachunki.txt wykonano.txt
```
6\. Utwórz plik wykonano.txt wielkości 11 bajtów, następnie podziel go pliki wielkości 5 bajtów. W ten sposób otrzymasz 3 pliki. (split)
```
cd temp



