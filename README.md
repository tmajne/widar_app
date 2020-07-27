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
            3. Status zamówienia
            4. Zamawiający (Dealer) => Relacja w przyszłości 
            5. Zamawiający (Handlowiec) => Relacja w przyszłości 
            6. Klient docelowy => Relacja w przyszłości
            7. Dane Podwozia => Relacja w przyszłości 
            8. Data złożenia zamówienia
            9. Data realizacji zamówienia
            10. Skąd przyjedzie podwozie
            11. Dokąd odstawić zabudowany pojazd
            12. Załączniki
            
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
                        - Dokładne dane produkcyjne (to temat na przyszłość)
                        - Wyposażenie dodatkowe
                        - Wymiary wewnętrzne zabudowy
                        - Termin realizacji 
                b) Na tej podstawie możemy utworzyć i połączyć następujące obiekty:
                    - Zamówienie (jako rekord w tabeli "Zamówienia")
                    - Handlowiec (relacja do rekordu w tabeli "Osoby" z rolą "Handlowiec"
                    - Podwozie (utworzenie rekordu i relacji z elementem w tabeli "Podwozia"
            2. Dostawa podwozia:
                a) Informacje które uzyskuje w momencie przyjęcia podwozia:
                    - Firma transportowa która przywiozła podwozie
                    - Imię i nazwisko kierowcy który przywiózł podwozie
                    - Data i godzina przek
                       
                    

    
    
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
