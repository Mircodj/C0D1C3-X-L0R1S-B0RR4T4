# Tools
### Ghidra
https://github.com/NationalSecurityAgency/ghidra/releases/tag/Ghidra_10.4_build
### OpenJDK
https://jdk.java.net/21/
### GEF
https://github.com/hugsy/gef
### Come installare Ghidra+JDK
1. Installare la release di Ghidra e usare il comando ``unzip nameZipFile.zip`` per unzipare la release di Ghidra
2. Unzippare il file ``openjdk.tar.gz`` mediante il comando ``tar -xvzf openjdk.tar.gz``
3. I passaggi UNO e DUE possono essere fatti anche mediante l'unzipper di sistema
4. Aprire la cartella di Ghidra (e, nel caso non ci fossero, dare i permessi a ``ghidraRun`` mediante il comando ``chmod +x ghidraRun``)
5. Runnare il binario ``ghidraRun``
6. Viene richiesto di selezionare il path di JDK > premere ``ENTER`` e selezionare la cartella ``openjdk`` (non la ``bin`` come in Windows)
### Cutter
https://cutter.re/

<hr>
<br>

# Comandi
### Comando fondamentale
<b>Ricordare SEMPRE</b> di dare i permessi al binario mediante ``chmod +x nomeBin``

### Cheatsheet per GEF e GDB by @zxgio
[Open file](./gdb_gef-cheatsheet.pdf)

<hr>
<br>

# Lista di comandi GEF e GDB By Espo
- ``break *main+<int>``: imposta il breakpoint a una riga del main. L'intero è individuabile tramite GEF affianco all'indirizzo di memoria di ogni singola istruzione ASM. Si può sostituire ``*main+<int>`` con un qualsiasi indirizzo di memoria dove sia posizionata una istruzione del binario
- ``run``: avvia il binario (e, nel caso di breakpoint impostato, runna fino al breakpoint stesso)
- ``si``: entra dentro alla funzione (quando viene callata)
- ``ni``: non entra dentro la funzione, ma la esegue e passa all'istruzione successivo
- ``start``: breakpoint a prima linea del main e run
- ``disassemble <symbol>``: mostra tutte le istruzioni del ``<symbol>``, dove <b>symbol</b> è il nome della funzione di nostro interesse.
- ``telescope``: vedere la memoria.
- ``info frame``: stampa indirizzo dello stack frame, registri salvati e i valori che hanno (<b>utile</b> per individuare l'indirizzo di ritorno e dove esso si trova (per effettuare overflow sull'indirizzo stesso))
- ``call (<retType>)<nameFunc>(<params>)``: serve per chiamare una funzione senza la necessità del supporto di main che esegue la stessa.
- ``checksec``: vedere le protezioni attive sul binario

<b>Feature di GDB</b>: una volta inserito un comando, se si preme enter senza digitare nulla viene reiterato il comando stesso.

# Nota del Merja
Mancano i writeup della 4a lezione della seconda parte e dell'ultimo es della 5a e l'integrazione con Mirco

# Come risolvere gli esercizi
Vi sono 5 categorie di esercizi:
- Reverse
- Patching
- Debugging
- Pwning
- Shellcode

<br>

Come le intende il prof:
- Static Analysis: ovvero senza necessità di patchare ma di analisi del ASM del binario
- Dynamic Analysis: analisi del ASM e patching dove serve, o u