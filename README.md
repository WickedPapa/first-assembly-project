# Conta i bit a 1 in Assembly (x86-64)

Questo progetto mostra un semplice programma in Assembly **x86-64 (GAS syntax)** che conta quanti bit impostati a 1 sono presenti in una variabile a 32 bit (`dato`).
Il risultato viene salvato nella variabile globale `conteggio`.

---

## ⚙️ Struttura dei file

```
conta-bit-a-uno.s   # Codice Assembly
test.c              # File C per testare la funzione Assembly
```

---

## 🚀 Esecuzione diretta (solo Assembly)

Compila e linka manualmente il file Assembly:

```bash
as conta-bit-a-uno.s -o conta-bit-a-uno.o
ld conta-bit-a-uno.o -o conta-bit-a-uno
```

Esegui:

```bash
./conta-bit-a-uno
```
---

## 🧪 Test tramite programma C

Puoi testare la funzione Assembly usando `test.c`, che la richiama e stampa il risultato.

Compila e linka insieme:

```bash
gcc conta-bit-a-uno.s test.c -o test
```

Esegui:

```bash
./test
```

Output atteso:

```
Conteggio = 10
```

---

## 💡 Note utili
* Per modificare il valore analizzato, cambia il contenuto di `dato` nella sezione `.data` del file Assembly.
