#### <mark style="background: #FFB86CA6;">**argparse.ArgumentParser(description="...")**</mark> - <mark style="background: #ABF7F7A6;">`init parser`</mark> - tworzy obiekt parsera; `description` dodaje opis programu widoczny przy wywołaniu pomocy (`-h`)

![[argp_instance.png](argp_img/argp_instance.png)

---

#### <mark style="background: #FFB86CA6;">**parser.parse_args()**</mark> - <mark style="background: #ABF7F7A6;">`execute parsing`</mark> - pobiera argumenty z terminala, przetwarza je i zwraca jako obiekt, w którym argumenty są atrybutami (np. `args.filename`)

![[parse_args](parse_args.png)