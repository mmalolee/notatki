#### <mark style="background: #FFB86CA6;">**sys.argv**</mark> - <mark style="background: #ABF7F7A6;">`argument values`</mark> - lista stringów zawierająca argumenty podane w terminalu; element `[0]` to zawsze nazwa uruchamianego skryptu

![argv.png](sys_img/argv.png)

---

#### **<mark style="background: #FFB86CA6;">sys.argv[n]</mark>** - <mark style="background: #ABF7F7A6;">`index access`</mark> - pobranie konkretnego argumentu z listy; `[1]` to pierwszy argument podany przez użytkownika

![argv_1.png](sys_img/argv_1.png)

---

#### <mark style="background: #FFB86CA6;">**sys.argv[1:]**</mark> - <mark style="background: #ABF7F7A6;">`list slicing`</mark> - wycina z listy nazwę skryptu, zostawiając tylko argumenty użytkownika; idealne do iteracji w pętli

![argv_slicing.png](sys_img/argv_slicing.png)

---

#### <mark style="background: #FFB86CA6;">**len(sys.argv)**</mark> - <mark style="background: #ABF7F7A6;">`length check`</mark> - dobra praktyka; sprawdza długość listy argumentów; służy do walidacji, czy użytkownik podał wymagane dane

![argv_len.png](sys_img/argv_len.png)

---

#### <mark style="background: #FFB86CA6;">**sys.exit()**</mark> - <mark style="background: #ABF7F7A6;">`system exit`</mark> - natychmiast przerywa działanie programu

![exit_code.png](sys_img/exit_code.png)
![[exit_out.png](sys_img/exit_out.png)

---

#### <mark style="background: #FFB86CA6;">**Iteracja pętlą for**</mark> - <mark style="background: #ABF7F7A6;">`argument loop`</mark> - pozwala obsłużyć wiele niezależnych flag w jednym uruchomieniu; przechodzimy przez listę argumentów i sprawdzamy każdy po kolei; możemy kombinować z logiką zmieniając/dodając ify

![argv_ify.png](sys_img/argv_ify.png)

---

#### **<mark style="background: #FFB86CA6;">sys.path</mark>** - <mark style="background: #ABF7F7A6;">`python path`</mark> - lista katalogów, w których Python szuka modułów do zaimportowania; jeśli Python "nie widzi" pliku `.py` w innym folderze, to tutaj szuka się ratunku; pierwszy element tej listy to ścieżka do pliku na którym pracujemy; jeżeli chcemy zaimportować jakiś pakiet skądś to musimy dodać do niego ścieżkę metodą `append()` do sys.path

![sys_path.png](sys_img/sys_path.png)

---

#### <mark style="background: #FFB86CA6;">**sys.executable**</mark> - <mark style="background: #ABF7F7A6;">`interpreter path`</mark> - ścieżka do pliku `.exe` (lub binarnego) Pythona, który aktualnie wykonuje kod; kluczowe, żeby sprawdzić, czy na pewno używasz swojego środowiska Conda, a nie systemowego Pythona

![executable.png](sys_img/executable.png)

---

