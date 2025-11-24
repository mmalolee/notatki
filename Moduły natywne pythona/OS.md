#### <mark style="background: #FFB86CA6;">**<mark style="background: #FF5582A6;">os.getcwd()</mark>** </mark>-  <mark style="background: #ABF7F7A6;">*get current working directory*</mark> - <mark style="background: #FFB86CA6;"></mark>zwraca STRINGA aktualnej ścieżki, na której pracujemy

![getcwd](os_images/getcwd.png)

---

#### <mark style="background: #FFB86CA6;">**os.chdir('*ścieżka `string`*')**</mark> - *<mark style="background: #ABF7F7A6;">change directory</mark>* - nic nie zwraca, zmienia jedynie ścieżkę, w której pracujemy; aby przejść katalog wyżej w argumencie należy podać dwie kropki

![chdir.png](os_images/chdir.png)

---

#### <mark style="background: #FFB86CA6;"> **os.listdir()**</mark> -<mark style="background: #ABF7F7A6;"> *list direction*</mark> - zwraca LISTĘ nazw plików z katalogu, w którym aktualnie się znajdujemy 

![listdir](os_images/listdir.png)

---

#### <mark style="background: #FFB86CA6;">**os.walk('*ścieżka `string`*')**</mark> - *<mark style="background: #ABF7F7A6;">przechodzić</mark>* - samo w sobie zwraca generator generujący krotkę/i z trzema wartościami; można przez nie przechodzić pętlą:
- pierwszy element to ścieżka do pliku:
 
![walk_root.png](os_images/walk_root.png)

- drugi to listy folderów:

![walk_directory.png](os_images/walk_directory.png)

- trzeci to listy plików w tych folderach:

![walk_file.png](os_images/walk_file.png)

---