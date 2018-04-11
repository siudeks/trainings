# trainings

Dokument w trakcie opracowywania
* Bezpieczne przechowywanie haseł w bazie danych
* rozsądne użycie metod http
* zrozumienie negocjacji protokołu (wywołanie długotrwających metod http nie zrównolegli się całkowicie - pierwsze wywołanie będzie trwało długo ponieważ 1) uzgadnia protokół 2) wywołuje długotrwale działającą operację)
* testy unitowe, integracyjne, findbugs


Opracowanie aplikacji w trzech krokach:
* Unit 0) Stworzenie aplikacji konsolowej do zarządzania biletami. Aplikacja będzie uruchomiona na stanowisku obsług klienta
* Unit 1) Stworzenie monolitu z logiką w endpointach i współdzielonym serwisem trzuymającym elementy w pamięci
* Unit 2) Przeniesienie zarządzania stanem do serwisu na zewnątrz do innego mikroserwisu
* Unit 3) Mikroserwis trzymający stan skonfigurować na trzymanie danych w bazie danych. Przyjrzeć się connection pool do bazy danych.
