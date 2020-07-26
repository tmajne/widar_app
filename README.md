# widar_app 

**I. Wstęp**

Aplikacja ma na celu uporządkowanie, wprowadzanie oraz archiwizowanie informacji produkcyjnych firmy Widar. 
    

**II. Wersje aplikacji**

## Widar App 0.1 - szablon graficzny + kilka pierwszych funkcji 

Cele:
- Aplikacja ma stworzony prosty interfejs graficzy. 
- Wyświetla po lewej stronie ekranu MENU z zakładą "Zamówienia", "Archiwum". 
- Po kliknięciu w "Zamówienia" zwraca rekordy z bazy "Zamówienia" 
- Lista umożliwia użytkownikowi możliwość wyświetlenia szczegółów zamówienia, edycję, usunięcie oraz archiwizację. 
- Na górze listy jest przycisk umożliwiający dodanie nowego zamówienia. Lista składa się z 7 kolumn:
            1. Kod zamówienia
            2. Status zamówienia
            3. Zamawiający (Dealer/Handlowiec)
            4. Model & Marka & Typ Podwozia
            5. VIN 
            6. VAN 
            7. Data realizacji
            8. Kolumna z opcjami
        
Po kliknięciu w szczegóły wyświetla się formularz który pobiera z bazy danych informacje o zamówieniu. Wszystkie potrzebne pola zostały opisane w "II. Baza danych". 
Po kliknięciu w przycisk "Zakończ" zamówienie przenosi się na listę "Archiwum"
Po kliknięciu na przycisk usuń zamówienie zostaje wykasowane z bazy danych. 

Docelowo mogłoby to wyglądać mniej więcej tak: https://sb-admin-pro-angular.startbootstrap.com/dashboard
    

**III. Baza Danych:** 

    1. Podwozia
        - Marka /string/
        - Model /string/
        - Typ podwozia /string/
        - VIN /string/
        - VAN /int/
        - Plac /bool/
        - Kolor /string/
        - Liczba miejsc /string/
        - Rozstaw osi /int/
        - Waga bez zabudowy /int/ 
        
    2. Dealerzy
        - Nazwa dealera (firmy);
        - NIP /int/
        - Adres/Ulica
        - Adres/Numer domu
        - Adres/Kod pocztowy
        - Adres/Miejscowość
        - Mail ogólny
    3. Handlowcy
        - Imię
        - Nazwisko
        - Numer kontaktowy 1
        - Numer kontaktowy 2
        - Email 
            RELACJE:
                => Podwozia
                => Dealer
                => Zamówienia
    4. Klienci docelowi
        - Nazwa firmy 
        - NIP
        - Adres/Ulica
        - Adres/Numer domu
        - Adres/Kod pocztowy
        - Adres/Miejscowość
        - Mail ogólny
        - Osoby (Relacja)

    5. Zamówienia
        - Numer zamówienia (wewnętrzny)
        - Numer zamówienia (zewnętrzny)
        - Zamawiający (Relacja=>Dealer)
        - Podwozie (Relacja)
        - Data zamówienia
        - Data realizacji
        - Handlowiec (Relacja)
        - Czy zakończono
        - Klient docelowy (Relacja)
        - Początkowe położenie podwozia (Czy przyjedzie z fabryki czy do odebrania od dealera)
        - Dokąd odstawić po zabudowaniu 
        Pliki: Skan zamówienia, Inne


    6. Osoby (z różnych firm)
        - Imię
        - Nazwisko
        - Telefon
        - Email
        - Firma (Relacja)
        - Rola (Właściciel, Kierowca, Pracownik biurowy, Handlowiec, Kierownik)
        - Opis roli (Doszczegółowienie)
        - 



    7. Zdarzenia
        - Przyjęcie zewnętrzne
        - Wydanie zewnętrzne 
        - Oddanie na produkcję
        - Przyjęcie poprodukcyjne
        - Wydanie zewnętrzne
        - Zadanie 
        - Zdarzenie 
        - Scheda (Uszkodzenie pojazdu)
 

    8. Zlecenia naprawy
        - Kod naprawy (1/ND/07/2020)
        - Obsługa zdarzeń (Przyjęcie zewnętrzne itp)
        - Zleceniodawca (Może być praktycznie każdy )
        - Pojazd (Relacja do bazy podwozi) - możliwość stworzenia nowego podwozia
        - Numer rejestracyjny
        - Zgłaszane rzeczy do naprawy 
        - Naprawy zrealizowane 
        - Stan licznika w momencie przekazania
        - Osoba zdająca pojazd do naprawy 
        - Osoba odbierająca pojazd z naprawy 
        - Stan paliwa (domyślnie "Brak danych")
        - Informacja o przypisanych pracownikach i ilości przepracowanych godzin
