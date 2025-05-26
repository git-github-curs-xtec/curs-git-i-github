# TA01: Git-LifeCycle

## Enunciat
Aquesta tasca la realitzarem fora de les pantalles usant la següent plantilla:

Hem creat un repo local des de zero que hem anomenat **chat-o-no-chat** i per fer-ho, hem les següents accions per ordre:
1. Per desplegar el repositori en una carpeta nova amb el nom donat: `git init chat-o-no-chat`
2. Per especificar qui està fent ús del repositori actualment: `git config --local user.name el-nostre-nom`
3. Per especificar el nostre email: `git config --local user.email el-nostre-email`
4. Creació de l'arxiu **chatgpt.py** amb el contingut:
``` python
def imprimir_frase():
    for _ in range(10):
        print("Si ens donguèssin el subsidi universal, què t'agradaria fer?")
```
2. Hem executat `git add chatgpt.py`
3. Hem creat l'arxiu **analogic.txt** amb el seguent contingut: "Llegir ens farà lliures"
4. Hem fet una còpia de l'arxiu **analogic.txt** i hem anomenat la còpia com a: **analogic_v2.txt**
5. Hem modificat l'arxiu **chatgpt.py** i ha quedat de la següent manera:
``` python
def imprimir_frase():
    for _ in range(10):
        print("Si ens donguèssin el subsidi universal, què t'agradaria fer?")

imprimir_frase()
```
6. Hem creat l'arxiu **examen.txt** i no li hem afegit cap contingut.
7. Hem executat `git add analogic.txt`
8. Hem executat `git add analogic_v2.txt`
9. Hem executat `git reset analogic.txt`
11. Hem creat el directori **/codi-enunciat** dins del l'arrel del repositori local
12. Hem executat `git commit -m "chore: afegir documents"` i ens ha generat el codi de commit **98900f3**
13. Hem creat un arxiu dins de **/codi-enunciat** i l'hem anomenat **exercici1.kt** amb el següent contingut:
```kotlin
fun imprimirFrase() {
    repeat(10) {
        println("Si ens donguèssin el subsidi universal, què t'agradaria fer?")
    }
}

fun main() {
    imprimirFrase()
}
```

- Quin serà l'estat del cicle de vida del fluxe de treball de repositori un cop fetes tote les accions anteriors?
- Quin serà el contingut confirmat de l'arxiu **chatgpt.py**?
- La carpeta **/codi-enunciat** estarà present a la zona confirmada del repositori local?

---
## Entrega
1. Escriu el nom dels arxius presents a cadascuna de les fases del cicle de vida del repositori en l'estat en què ha quedat. També pots dibuixar.
2. Respon i argumenta les preguntes anteriors.
