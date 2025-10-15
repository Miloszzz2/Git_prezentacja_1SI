# Git – Podstawy i Praktyka

## Czym jest Git?
Git to **rozproszony system kontroli wersji** stworzony przez Linusa Torvaldsa w 2005 roku.  
Umożliwia śledzenie zmian w plikach, cofanie do wcześniejszych wersji i bezpieczną współpracę zespołową.  
Każdy programista ma pełną kopię repozytorium – można pracować **offline**.

### Zalety:
- szybki i wydajny  
- działa offline  
- zapewnia integralność danych  
- obsługuje gałęzie (branching)  
- kompatybilny z wieloma protokołami  

---

## Kluczowe pojęcia

- **Repozytorium** – historia projektu i wszystkie jego pliki  
- **Commit** – zapis zmian z opisem  
- **Branch (gałąź)** – równoległa wersja rozwoju  
- **Merge** – łączenie zmian z różnych gałęzi  

### Trzy obszary Gita
1. **Working Directory** – pliki, nad którymi pracujesz  
2. **Staging Area** – przygotowane do zapisu zmiany  
3. **Repository** – zapisane commity  

---

## Najważniejsze komendy

```bash
git init       # utwórz repozytorium
git add .      # dodaj zmiany do staging area
git commit -m "Opis zmian"  # zapisz zmiany
git status     # sprawdź status
git log        # pokaż historię commitów
```

---

## Praca zdalna

| Komenda | Działanie |
|----------|------------|
| git clone | pobiera repozytorium |
| git push | wysyła zmiany do repozytorium zdalnego |
| git pull | pobiera i scala zmiany |
| git fetch | pobiera zmiany bez scalania |
| git remote | zarządza repozytoriami zdalnymi |

Popularne platformy: **GitHub**, **GitLab**, **Bitbucket**

---

## Konflikty i ich rozwiązywanie
Konflikt pojawia się, gdy dwie osoby zmieniają ten sam fragment kodu.  
Aby go rozwiązać:
1. Otwórz plik i znajdź znaczniki konfliktu  
2. Wybierz właściwą wersję  
3. Zapisz plik i wykonaj `git add`, potem `git commit`

### Jak unikać konfliktów:
- często aktualizuj gałąź (`git pull`)  
- rób małe commity  
- komunikuj się z zespołem  

---

## Zaawansowane funkcje

- **Rebase** – porządkuje historię commitów  
- **Cherry-pick** – wybiera pojedynczy commit z innej gałęzi  
- **Stash** – tymczasowo odkłada zmiany  
- **Reset** – cofa historię (usuwa zmiany)  
- **Revert** – tworzy commit cofający poprzedni  

---

## GitHub – najpopularniejsza platforma
Funkcje:
- **Pull Requests** – przegląd i dyskusja nad zmianami  
- **Issues** – zgłaszanie błędów i zadań  
- **Actions** – automatyzacja CI/CD  
- **Pages** – hosting stron  
- **Security** – skanowanie i ochrona kodu  

Dla studentów: **GitHub Student Developer Pack** (darmowe narzędzia, m.in. Copilot).

---

## Bezpieczeństwo

### Ryzyka:
- przypadkowe ujawnienie haseł lub kluczy  
- brak 2FA  
- złośliwy kod w repozytorium  

### Dobre praktyki:
- używaj `.gitignore` dla plików z danymi wrażliwymi  
- stosuj **zmienne środowiskowe**  
- używaj **menedżerów sekretów** (Vault, AWS Secrets Manager)  
- włącz **uwierzytelnianie dwuskładnikowe**

Przykład `.gitignore`:
```
.env
config.json
*.key
*.log
tmp/
```

---

## Git i sztuczna inteligencja

### Wyzwania:
- duże pliki → użyj **Git LFS**  
- wersjonowanie modeli → **DVC**, **MLflow**  
- śledzenie eksperymentów → dedykowane narzędzia AI  

### Narzędzia:
- **GitHub Copilot** – AI asystent kodu  
- **OpenCommit / GitKraken AI** – generowanie komunikatów commitów  
- **DVC** – wersjonowanie danych i modeli  

---

## Najlepsze praktyki

### Commitowanie:
- commituj często i małe zmiany  
- pisz jasne wiadomości (np. `feat: dodaj logowanie`)  

### Praca z gałęziami:
- osobna gałąź dla każdej funkcji  
- utrzymuj czystą gałąź główną (`main`)  
- usuwaj nieużywane gałęzie  

### Zespół:
- używaj **pull requestów** i **issues**  
- dokumentuj zmiany  
- komunikuj się z zespołem  

### Automatyzacja:
- używaj **Git hooks**  
- integruj z **CI/CD**  
- korzystaj z narzędzi graficznych (GitKraken, SourceTree)  
