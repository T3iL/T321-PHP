# T321-PHP

1. PHP recap ($, ARRAYS, ARRAYS assoc)
2. SORT, ASORT, KSORT
3. INCLUDE/REQUIRE include 'file_name'; include_once 'file_name'; [info](https://www.w3schools.com/php/php_includes.asp)
4. Zmienne globalne ARRAYS
5. EXPLODE
6. COUNT
7. IF, SWITCH, FOR, FOREACH, WHILE

```
ZADT32101.
Przygotuj tablicę uzytkowników w PHP pobranych z 
https://jsonplaceholder.typicode.com/users 
i wypisz ją na ekranie (zamień rekordy JSON na tablicę PHP) - name,username,email

ZADT32102.
Posortuj tablicę $persons utworzoną z poniższych danych: 

Krzysztof":PL
John":US
Mirriam":SK
Mary":GB
Santiago":AR
Enrique:ES

a następnie osortuj wg elementów i wg kluczy

ZADT32103. 
Przygotuj aplikację wyświetlającą inne pozdrowienie w zależności od podanej pory dnia (switch)

ZADT32104.
Wypisz sformatowane dane z zadania 1 w postaci tabeli HTML zawierającej:
przykład

```

|Imię:   | Leanne Graham                                  |
|--------|------------------------------------------------|
|email:  | Sincere@april.biz                              |
|addres: | Kulas Light, Apt. 556, Gwenborough, 92998-3874 |
```
ZADT32105.
Połącz się ze zdalnym kontem FTP (poniżej uprawnienia), 
utwórz katalog nazwany własnym imieniem 
i prześlij tam wszystkie wykonane ćwiczenia

ZADT32106. 
Przygotuj szablon witryny z menu składającej się czterech podstron 
(HOME,SERVICES,ABOUT,CONTACT) 
korzystających z tego samego nagłówka i stopki 

ZADT32105.
Zmień CSS w elemencie menu na podstawie URL strony (zmiana tła)

ZADT32107.
Przygotuj funkcję zamieniającą kilometry na mile

ZADT32108.
Zapamiętaj poprzednio odwiedzona strone z zad 4 za pomocą cookies i/lub sesji

ZADT32109.
Wyświetl na stronie treść tekstu zapisaną w pliku rtf

ZADT32109.
Przygotuj formularz rejestracyjny i wypisz na stronie wysłane z niego dane (input/textarea/select/radio/checkbox/file)

ZAD32110.
Przygotuj treść gry RPG w pliku txt

[1,0,2]:Za górami za lasami był wielki las. W tym lesie spotykasz różne postaci.
[2,0,0]:Spotykasz trolla. Co robisz
[3,1,4]:Walczysz z nim
[3,2,5]:Uciekasz
[3,3,9]:Wdajesz się w rozmowę
[4,0,0]:Wybierz broń
[4,1,6]:Miecz
[4,2,7]:Łuk
[4,3,8]:Wulgaryzmy
[5,0,101]:Wpadasz do bagna
[6,0,101]:Zapomniałeś miecza
[7,0,101]:Nie masz juz strzal
[8,0,200]:Pokonujesz trolla
[9,0,10]:Zaczynacie rozmowe:
[10,1,102]:Mówisz mu że jesteś smaczny
[10,2,102]:Pytasz o drogę
[10,3,103]:Grozisz mu że wrócisz z kumplami
[100,0,1]:Koniec gry (giniesz w męczarniach)
[101,0,1]:Giniesz w bagnie
[101,0,1]:Giniesz zjedzony
[102,0,200]:Wskazuje ci bezpieczną drogę i odchodzisz
[103,0,100]:Woła swoich kumpli i to już ne kończy się dobrze
[200,0,0]:Gratulacje, pokonałeś wszystkich przeciwników!
```

### --------Konto FTP
![FTP](/kontoFTP.PNG)

12Technik!"

[PHP: Reading the "clean" text from RTF](https://webcheatsheet.com/php/reading_the_clean_text_from_rtf.php)

[STACKOVERFLOW - read word document in php](https://stackoverflow.com/questions/10646445/read-word-document-in-php)

```php
function read_docx($filename){

    $striped_content = '';
    $content = '';

    if(!$filename || !file_exists($filename)) return false;

    $zip = zip_open($filename);
    if (!$zip || is_numeric($zip)) return false;

    while ($zip_entry = zip_read($zip)) {

        if (zip_entry_open($zip, $zip_entry) == FALSE) continue;

        if (zip_entry_name($zip_entry) != "word/document.xml") continue;

        $content .= zip_entry_read($zip_entry, zip_entry_filesize($zip_entry));

        zip_entry_close($zip_entry);
    }
    zip_close($zip);      
    $content = str_replace('</w:r></w:p></w:tc><w:tc>', " ", $content);
    $content = str_replace('</w:r></w:p>', "\r\n", $content);
    $striped_content = strip_tags($content);

    return $striped_content;
}
```

### --------Repositiories

https://www.php.net/manual

https://miroslawzelent.pl/kurs-html/pozostale-kontrolki-formularzy/

https://miroslawzelent.pl/kurs-php/

http://www.newthinktank.com/2019/12/learn-php-one-video/

https://youtu.be/2eebptXfEvw

### --------On line editor
PHP: https://sandbox.onlinephpfunctions.com/
### ---------Assets
https://cdnjs.com/ | https://fontawesome.com | http://fontello.com/ | https://fonts.google.com/ |
### ---------Stock Img
https://www.pexels.com/ | https://unsplash.com | https://pixabay.com
### ---------Licence
[MIT](https://choosealicense.com/licenses/mit/)


