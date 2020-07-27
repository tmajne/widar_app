# widar_app 

## I. Wstęp

Aplikacja ma na celu uporządkowanie, wprowadzanie oraz archiwizowanie informacji produkcyjnych firmy Widar. 
    

## II. Wersje aplikacji

### Widar App 0.1 - szablon graficzny + kilka pierwszych funkcji 

#### Cele:
- Aplikacja ma stworzony **prosty interfejs** graficzy. 
- Menu: **Zamówienia** 
- Widok **listy zamówień**
- Widok **edycji**
- Widok **podglądu** 
- Aplikacja umożliwia użytkownikowi możliwość wylistowania, wyświetlenia szczegółów, edycję oraz usunięcie zamówienia. 
- Na górze listy jest przycisk umożliwiający dodanie nowego zamówienia. Lista składa się z 7 kolumn:
            1. Kod zamówienia
            2. Numer zamówienia (zewnętrzny)
            2. Status zamówienia
            3. Zamawiający (Dealer) => Relacja w przyszłości 
            4. Zamawiający (Handlowiec) => Relacja w przyszłości 
            5. Klient docelowy => Relacja w przyszłości
            6. Dane Podwozia => Relacja w przyszłości 
            7. Data złożenia zamówienia
            8. Data realizacji zamówienia
            9. Skąd przyjedzie podwozie
            10. Dokąd odstawić zabudowany pojazd
            11. Załączniki
            
            Etapy zamówienia:
            1. Wpłynięcie zamówienia do firmy 
                a) Informacje które zawiera zamówienie:
                    - Data złożenia zamówienia
                    - Handlowiec
                    - Numer zamówienia (zewn)
                    - Rodzaj zabudowy
                    - Model Marka Typ
                    - rozstaw osi 
                    - VIN lub VAN podwozia
                    - Skąd przyjedzie podwozie
                    - Gdzie dostarczyć po zabudowie
                    - Specyfikacja zabudowy
                        - Skrócona nazwa opisowa zabudowy np. MaxTrans FLP RD => legenda
                        - 
                        - Termin realizacji 
                    

    
    
### Widar App 0.2 - rozbudowanie funkcji 

#### Cele:

## III. Baza Danych:

    1. Podwozia
Marka /string/ | Model /string/ | Typ podwozia /string/|VIN  | VAN | Plac |Kolor | Liczba miejsc | Rozstaw osi| Waga bez zabudowy|
---------------|----------------|----------------------|-----|-----|------|------|---------------|------------|------------------|
Lorem ipsum    | Lorem ipsum    | Lorem ipsum          |Lorem|Lorem|Lorem |Lorem |Lorem ipsum    | Lorem      |                  |

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
        - Przyjęcie poprodukcyjne (
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
