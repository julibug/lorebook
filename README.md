# 📚 Lorebook

Aplikacja webowa dla pisarzy do porządkowania świata powieści — postacie, bestiariusz, plan wydarzeń, miejsca i notatki, z obsługą wielu książek i synchronizacją między urządzeniami na żywo.

> Projekt powstał jako narzędzie do pracy nad moją własną powieścią o wampirach. 🦇

## ✨ Funkcje

- **Wiele książek** — po zalogowaniu wybierasz książkę z listy; każdą można dodać, zmienić jej tytuł lub usunąć, a każda ma całkowicie osobne dane
- **Kartoteka postaci** — imię, moce, opis i zdjęcie każdej postaci
- **Bestiariusz** — katalog stworzeń zamieszkujących świat powieści
- **Plan wydarzeń (Outline)** — rozdziały z listą wydarzeń, układane przeciąganiem (drag & drop)
- **Miejsca** — lokacje z notatkami i galerią zdjęć
- **Notatki** — szybkie zapiski z wyszukiwarką
- **Ostatnie zmiany** — dziennik aktywności pokazujący, co ostatnio edytowano

## 🔄 Synchronizacja i bezpieczeństwo

- **Logowanie** (Firebase Authentication, e-mail + hasło) — dane widzi tylko zalogowany właściciel
- **Synchronizacja na żywo** (Firebase Realtime Database) — zmiana zapisana na komputerze pojawia się na telefonie w kilka sekund, i odwrotnie
- **Tryb offline** — dane zapisują się też lokalnie w przeglądarce, więc aplikacja działa bez internetu
- **Reguły dostępu** w bazie danych ograniczają odczyt i zapis wyłącznie do konta właściciela
- Zdjęcia są automatycznie zmniejszane przed zapisem, żeby oszczędzać miejsce

## 🛠 Technologie

| Warstwa | Rozwiązanie |
|---|---|
| Frontend | HTML + CSS + czysty JavaScript (jeden plik, zero frameworków) |
| Logowanie | Firebase Authentication |
| Baza danych | Firebase Realtime Database |
| Hosting | GitHub Pages |

Całość mieści się w pojedynczym pliku `index.html` — bez procesu budowania, bez zależności do instalowania. Interfejs aplikacji jest w języku angielskim, a układ dostosowuje się do ekranu telefonu.

## 🚀 Uruchomienie

Aplikacja działa pod adresem GitHub Pages tego repozytorium. Bez zalogowania widoczny jest tylko ekran logowania — treści są prywatne.

Aby uruchomić własną kopię:

1. Sklonuj repozytorium i utwórz darmowy projekt w [Firebase](https://console.firebase.google.com) (plan Spark).
2. Włącz **Authentication** (e-mail/hasło) i dodaj użytkownika.
3. Utwórz **Realtime Database** z regułami ograniczającymi dostęp do `users/$uid`.
4. Wklej swoją konfigurację `firebaseConfig` w `index.html`.
5. Opublikuj plik na dowolnym hostingu statycznym (np. GitHub Pages).
