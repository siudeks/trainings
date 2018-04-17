# Inspiracje

* Reaktywność
* REST
* Spring
* Bazy danych
* Skalowalność

## Część 1

Czołem programisto! Nasz nowy klient CIT (Centrum Informacji Turystycznej) chce mieć aplikację która będzie wykorzystywana do rejestracji uczestników na organizowane wydarzenia.  
Na obecnym etapie aplikacja będzie zainstalowana lokalnie w siedzibie CIT i obsługiwana wyłącznie przez operatora. Prosty interfejs znakowy wystarczy w zupełności do obsługi programu przez jedynego uzytkownika.
Operator chce:
* rejestrować uczestników na konkretne wydarzenia
* rejestrować opiekunów tych wydarzeń

Zadanie:
* Skonstruuj listę funkcjonalności które chcesz dostarczyć w aplikacji
* napisz aplikację



-----
Pomysły na później:

* Bezpieczne przechowywanie haseł w bazie danych
* rozsądne użycie metod http
* zrozumienie negocjacji protokołu (wywołanie długotrwających metod http nie zrównolegli się całkowicie - pierwsze wywołanie będzie trwało długo ponieważ 1) uzgadnia protokół 2) wywołuje długotrwale działającą operację)
* testy unitowe, integracyjne, findbugs


Opracowanie aplikacji w trzech krokach:
* Unit 1) Stworzenie monolitu z logiką w endpointach i współdzielonym serwisem trzuymającym elementy w pamięci
* Unit 2) Przeniesienie zarządzania stanem do serwisu na zewnątrz do innego mikroserwisu
* Unit 3) Mikroserwis trzymający stan skonfigurować na trzymanie danych w bazie danych. Przyjrzeć się connection pool do bazy danych.
