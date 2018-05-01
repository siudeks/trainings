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
* rejestrować uczestników na konkretne wydarzenia tak, aby wiedzieć czy osiągnięto minimalną ilość uczestników lub nie przekroczono maksymalnej ilości uczestników (powstaje wtedy lista rezerwowa)
* rejestrować opiekunów tych wydarzeń

Zadanie 1:
* Skonstruuj listę funkcjonalności które chcesz dostarczyć w aplikacji
* napisz aplikację
* rewykorzystaj model bazy danych w komunikacji DAO tak aby w przyszłym refaktoerze potem widzieć sens separacji modeli
* stwórz model UI z opcjami wybory i skonstruuj odpowiadającą mu tabelę tak, aby potem widzieć zapytania badające warunki OR i AND na indywidualnych kolumnach tabeli



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

Inne:
* Użycie lomboka w encjach
Podsumowanie:
1.	Zmiana API np.:
Get->/user/{userId}
Put->/user/{userId} {body}
Post->/discount {body}
Put->/discount {body} 
Delete->/discount/{(type} 
Get->/discount/{type}
2.	 Stworzenie packagu z encjami

1. relacja wiele do wielu miedzy film a room
2. dodanie czasu wyswietlania filmu
3. Zaprojektowanie API

1. Dodanie metody w controllerze zwracjacej typ ResponseEntity<JakisObject>
2. Testy integracyjne dla obu metod(ResponseEntity<JakisObject> i JakisObject) za pomocą klasy TestRestTemplate
3. Przejrzenie roznic miedzy 4 metodami protokolu http(get,post,delete,put) z wyjasniem które sa safe i idempotent i w jakich sytuacjach powinny być używane

Podsumowanie:
Step 0:
Stworzenie aplikacji „hello world” za pomocą Springa, mavena, która zwroci String „hello world” za pomocą metody GET. Do manualnego testu można uzyc pluginu do przeglądarki Postman.

http://localhost:8080/api/hello <- zwroci Stringa

Prawdopodobny stack technologiczny:
Java 8, SpringBoot 2, Maven, MySql, Git, JUnit + AssertJ, Mockito, Lombok, Guava, Slf4j by Lombok

1.	drobne poprawki API
2.	poprawa encji, poczytanie o cascadeType, fetchType, orphanRemoval
3.	opcjonalnie -> testy kaskadowosci i orphanRemoval za pomoca h2


Wykonaj listener jako:
* klasę wewnętrzną
* klasę zewnętrzną
* klasę lokalną
* klasę anonimową


caching in spring

