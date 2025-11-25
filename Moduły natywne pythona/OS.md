#### <mark style="background: #FFB86CA6;">**<mark style="background: #FF5582A6;">os.getcwd()</mark>** </mark>-  <mark style="background: #ABF7F7A6;">*get current working directory*</mark> - <mark style="background: #FFB86CA6;"></mark>zwraca STRINGA aktualnej ścieżki, na której pracujemy

![getcwd](os_images/getcwd.png)

---

#### <mark style="background: #FFB86CA6;">**os.chdir('*ścieżka `string`*')**</mark> - *<mark style="background: #ABF7F7A6;">change directory</mark>* - nic nie zwraca, zmienia jedynie ścieżkę, w której pracujemy; aby przejść katalog wyżej w argumencie należy podać dwie kropki

![chdir.png](os_images/chdir.png)

---

#### <mark style="background: #FFB86CA6;"> **os.listdir()**</mark> -<mark style="background: #ABF7F7A6;"> *list direction*</mark> - zwraca LISTĘ nazw plików i folderów z folderu, w którym aktualnie się znajdujemy 

![listdir](os_images/listdir.png)

---

#### <mark style="background: #FFB86CA6;">**os.walk('*ścieżka `string`*')**</mark> - *<mark style="background: #ABF7F7A6;">przechodzić</mark>* - samo w sobie zwraca generator generujący krotkę/i z trzema wartościami; można przez nie przechodzić pętlą:

- #### pierwszy element to ścieżka do aktualnie przetwarzanego folderu:
 
![walk_root.png](os_images/walk_root.png)

- #### drugi to listy folderów:

![walk_directory.png](os_images/walk_directory.png)

- #### trzeci to listy plików w tych folderach:

![walk_file.png](os_images/walk_file.png)
#### Można dodawać warunki w pętli, np. odfiltrować puste listy, albo przejść wewnętrzną pętlą przez listy i dodać warunki czy dany element listy zawiera jakiś konkretny ciąg znaków:

![walk_filtrowanie](os_images/walk_filtrowanie.png)

#### Kombinując z roots i files można łatwo wygenerować sobie ścieżki do wszystkich plików:

![walk_tworzeniesciezekdoplikow](os_images/walk_tworzeniesciezekdoplikow.png)

---

#### <mark style="background: #FFB86CA6;">**os.mkdir('*nazwa_folderu `string`*')**</mark> - <mark style="background: #ABF7F7A6;">*make directory*</mark> - tworzy folder  w katalogu, w którym aktualnie się znajdujemy (tylko jeden)

![mkdir](os_images/mkdir.png)

---

#### <mark style="background: #FFB86CA6;">**os.makedirs('*nazwy_folderów_jako_ścieżka `string`*')**</mark> - *<mark style="background: #ABF7F7A6;">make directories</mark>* - to samo co poprzednik, z tą różnicą, że może tworzyć zagnieżdżone struktury

![makedirs](os_images/makedirs.png)

---

#### **<mark style="background: #FFB86CA6;">os.rmdir('*nazwa_folderu `string`*)</mark>** - *<mark style="background: #ABF7F7A6;">remove directory</mark>* - usuwa folder z katalogu, na którym aktualnie pracujemy (tak samo jak w mkdir, usunie tylko jeden, aby usunąć więcej należy użyc <mark style="background: #FFB86CA6;">**os.removedirs('*nazwy_folderów_jako_ścieżka `string`*)**</mark> - *<mark style="background: #ABF7F7A6;">remove directories</mark>*)

---

<mark style="background: #FFB86CA6;">**os.rename('nazwa_do_zmiany', 'nazwa_na_którą_zmieni' `string`)**</mark> - <mark style="background: #ABF7F7A6;">*przezwij*</mark> - zmienia nazwę folderu o podanej nazwie na nazwę podaną w drugim argumencie

![rename](os_images/rename.png)

---

#### **os.stat('nazwa_pliku' `*string*`)** - *statistics* - zwraca obiekt klasy, który opisuje statystyki pliku, którego nazwa została przekazana w argumencie

| **Atrybut**      | **Opis**                                                                                                                                                                                         |
| ---------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **`st_mode`**    | Tryb ochrony pliku (np. uprawnienia i typ pliku, np. katalog, zwykły plik). Jest to pole bitowe.                                                                                                 |
| **`st_ino`**     | Numer **i-węzła** (inode) urządzenia, na którym znajduje się plik.                                                                                                                               |
| **`st_dev`**     | Identyfikator urządzenia, na którym plik jest rezydentny.                                                                                                                                        |
| **`st_nlink`**   | Liczba twardych (trwałych) dowiązań do pliku.                                                                                                                                                    |
| **`st_uid`**     | Identyfikator użytkownika (User ID - **UID**) właściciela pliku.                                                                                                                                 |
| **`st_gid`**     | Identyfikator grupy (Group ID - **GID**) właściciela pliku.                                                                                                                                      |
| **`st_size`**    | Rozmiar pliku w **bajtach**. Dla niektórych typów plików (np. FIFO, gniazda) znaczenie może być inne.                                                                                            |
| **`st_atime`**   | Czas **ostatniego dostępu** do pliku, wyrażony jako liczba sekund od Epoki (zazwyczaj 1 stycznia 1970).                                                                                          |
| **`st_mtime`**   | Czas **ostatniej modyfikacji** zawartości pliku, wyrażony w sekundach od Epoki.                                                                                                                  |
| **`st_ctime`**   | Czas **ostatniej zmiany metadanych** pliku (np. uprawnień, właściciela) w systemach uniksopodobnych (np. Linux) lub **czas utworzenia** pliku w systemie Windows, wyrażony w sekundach od Epoki. |
| **`st_blocks`**  | (Dostępne na niektórych systemach) Liczba bloków po 512 bajtów przydzielonych dla pliku.                                                                                                         |
| **`st_blksize`** | (Dostępne na niektórych systemach) Preferowany rozmiar bloku dla operacji wejścia/wyjścia.                                                                                                       |
| **`st_rdev`**    | (Dostępne dla plików specjalnych urządzeń) Identyfikator urządzenia, jeśli plik jest plikiem specjalnym urządzenia (blokowym lub znakowym).                                                      |

---

#### **os.environ['klucz' *`string`*]** - *environment* - obiekt, który zachowuje się jak słownik i przechowuje zmienne środowiskowe. 

![environ_items!](environ_items.png)

Za jego pomocą można pobierać zmienne z pliku `.env` bezpośrednio albo za pomocą metody **get()**

![env_api1_directly](os_images/env_api1_directly.png)

---

os.path.basename('sciezka')

![path_basename.png](os_images/path_basename.png)

---

os.path.dirname('sciezka')

![path_dirname.png](os_images/path_dirname.png)

---

os.path.split('ścieżka)

![[path_split.png]]