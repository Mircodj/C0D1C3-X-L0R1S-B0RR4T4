# Funzioni a caso

### Shifting di una stringa "abc" -> "cde"

```python
input = 'abc'
key = 2
output = ''

for c in input:
    output += chr(ord(c) + key)
print(output)
```

-------------------------

### Generazione stringa random

```python
import random
import string


vocabulary = list(string.ascii_letters) + list(string.digits)
pass = ""
size = 10

for i in range(size):
    random.shuffle(vocabulary)
    pass += vocabulary[0]
print(f"Password: {password}")
```

```python
import random
import string

letters = string.ascii_lowercase

def get_random_string(length):
    result_str = ''.join(random.choice(letters) for i in range(length))
    return result_str

print(get_random_string(8))
```

-------------------------

### Prendere tutti caratteri maiuscoli da file

```python
file1 = open('input.txt', 'r')
lines = file1.readlines()

out = ""
for linea in lines:
    linea = linea.strip()
    for char in linea:
        if ord(char)>64 and ord(char)<=64+32:
            out += char

print(out)
```

-------------------------

### Decodifica da base64 a stringa

```python
import base64
 
b64 = "fYZ7ipGIjFtsXpNLbHdPbXdaam1PS1c5lQ=="
bytes = base64.b64decode(b64)
stringa = bytes.decode("UTF-8")
```

-------------------------

### Bruteforce Cesare da Base64

```python
import base64
 
b64 = "INSERIRE QUI IL BASE64=="
bytes = base64.b64decode(b64)

for i in range (0, 256):
    for byte in bytes:
        print(chr((byte+i)%256), end="")
    print(" ")
```

--------------------

### Decodifica cifrario di Vigenere
<https://www.dcode.fr/vigenere-cipher>

--------------------

### Decodifica cifrario a sostituzione (Substitution)
<https://www.guballa.de/substitution-solver>

--------------------

### Sito per md5, sha1, sha256 ecc...
<https://crackstation.net/>

<https://www.tunnelsup.com/hash-analyzer/>

--------------------

### SQL Injection

```
' OR 1='1
' or 1=1--
```

------------------

### CRLF Attack

```
if an attacker can execute the CRLF attack, he can fake the log content
/index.php?page=home& %0d%0a 127.0.0.1 - 08:15 - /index.php?page=home&restricredredactio=edi
```

------------------

### OS Command Injection Attack

```
http://example.com/ping.php?address=8.8.8.8 %26ls
Note that 26 -> &
```

--------------

### XOR ripetuto con LEN(S1) > LEN(S2)

```python
import string

alph = list(string.ascii_uppercase)
f = open("encrypted", "r").readline()

def customXOR(text, key):
    out = ""
    for i in range(0, len(text)):
        out += (chr( ord(text[i]) ^ ord(key[i%2])))
    return out
                 
for a in alph:
    for b in alph:
        key = a+b
        if "spritz" in customXOR(f, key) : print(customXOR(f, key))
```

------------------------

###  Rimpiazzo caratteri in stringhe

```python
string = "Palle"
new_string = string.replace("e", "a") 
  
print(new_string)   #STAMPA: "Palla"
```

------------------------

### String Interpolation

```python
'%s is smaller than %s' % ('one', 'two')

print("Mr. %s, the total is %.2f." % ("Jekyll", 15.53))
'Mr. Jekyll, the total is 15.33.'

>>> place = "New York"
>>> print("Welcome to %s!" % place)
Welcome to New York!

palle = {"allowed_flag":"sos", "palle1":"palle2"}
str = "flag: %(allowed_flag)s" % palle
print(str)     #stampa "flag: sos"
```