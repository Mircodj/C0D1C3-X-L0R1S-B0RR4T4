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

# Nota del Merja
Mancano i writeup della 4a lezione della seconda parte e dell'ultimo es della 5a e l'integrazione con Mirco