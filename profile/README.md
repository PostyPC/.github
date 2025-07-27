## Hi there 👋

<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->

# PostyPC – NX Post Configurator Repositories

Witamy w organizacji **PostyPC**, gdzie zarządzamy postprocesorami NX w strukturze wielu repozytoriów.

---

## 🛠️ Nasz workflow pracy z postprocesorami

### 1. Repozytoria Git

- Każdy postprocesor ma własne, oddzielne repozytorium w organizacji PostyPC.
- Repozytoria zawierają pliki źródłowe postprocesorów oraz plik `version.txt` do śledzenia wersji.
- W repozytoriach ignorujemy pliki `.prt` oraz inne ciężkie pliki CAD (zdefiniowane w `.gitignore`).

### 2. Tworzenie i dystrybucja paczek na NAS

- Finalne paczki postprocesorów, zwykle zawierające kilka postów, są tworzone jako archiwa ZIP na serwerze NAS.
- Wersje paczek na NAS oznaczamy w formacie `vX.YY`, gdzie:
  - `X` – liczba unikalnych postprocesorów w paczce
  - `YY` – numer kolejnej wersji paczki
- Nawet jeśli nie wszystkie posty zostały zmienione, dla prostoty wysyłamy całą paczkę.

### 3. Współpraca zespołowa

- Programiści mogą pracować lokalnie na repozytoriach Git, tworząc branch’e i wykonując commity.
- Aby zaktualizować wersję paczki na NAS:
  - Klonujemy odpowiednie repozytoria
  - Tworzymy branch dla nowej wersji
  - Kopiujemy zawartość paczki z NAS do lokalnego repo
  - Wprowadzamy zmiany i commitujemy
  - Pushujemy zmiany do zdalnego repozytorium
- Następnie generujemy nową paczkę ZIP i uploadujemy ją na NAS z nowym tagiem wersji.


