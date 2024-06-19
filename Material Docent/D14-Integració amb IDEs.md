# Integració amb IDEs
La gran majoria d'IDEs es sincronitzen amb Git ja sigui directament o a través de plugins.

---
## Integració IntelliJ IDEA
IntelliJ és un IDE de IDEA JetBrains pensat per a projecte de Java, Kotlin i similars que permet integració amb Git de forma nativa.

Per a fer-ho, creem projecte nou normalment i escollim crear repo Git:
![](img/Pasted%20image%2020240619172917.png)

Per exemple escollim projecte de **Kotlin**:
![](img/Pasted%20image%2020240619173006.png)

Com que hem escollit que creeï codi de demo, ja ens ha fet un primer commit en una branca `main` per defecte:
![](img/Pasted%20image%2020240619173108.png)
Fins i tot ens ha creat un arxiu `.gitignore`!

Al **Menú principal/Git** hi tenim totes les comandes previstes per Git:
![](img/Pasted%20image%2020240619173201.png)

Si xafardagem, hi trobarem moltes comandes que ja coneixem; per exemple també ens apareix l'opció de Clone, Merge, Commit, Push, Pull...

>[!TIP]
>Per a vincular el nostre repo local creat amb un repo remot, podem fer-ho a través de **Manage Remotes...** i enganxar la URL del nostre repo remot: 
>![](img/Pasted%20image%2020240619173339.png)

>[!WARNING]
>Si el nostre repo local té un **històric de commits** diferent del repo remot, no podrem sincronitzar-los. Per tal d'evitar aquestes situacions, l'ideal és que: o bé creem el repo remot des de GitHub i el tenim buit sense cap commit; o bé creem el repo des de GitHub i el clonem al local.

També podem desplegar un repo local de Git sobre un projecte que ja tinguem a mitges:
![](img/Pasted%20image%2020240619173750.png)

---

## Integració Visual Studio Code (VSC)
Visual Studio Code és un IDE **lleuger** i **multipropòsit** que també compleix la funció d'editor de text avançat gràcies a la seva multitud de plugins.

Hi podem desenvolupar projectes web amb php, html, css, xml amb qualsevol framework; però també java, python; visualtizar arxius json, csv, etc...

**Té plugins per a fer qualsevol** cosa inclús visualitzar arxius pdf i excel?

Per a usar-lo amb integració amb Git, es recomana instal·lar el plugin anomenat **GitHub Pull Requests** que és l'oficial proveït per GitHub.
![](img/Pasted%20image%2020240619174700.png)

>[!TIP]
>Com podem veure, també incorpora el plugin de **GitHub Copilot** que ens permetrà desenvolupar codi automàticament. *(Serà necessari tenir un compte de GitHub PRO o GitHub Education)*.

Un cop instal·lat, ens apareix l'icona que simula tres punts de commit en dues branques i allà s'ens despleguen les opcions de Git:
![](img/Pasted%20image%2020240619174643.png)

Podem veure les **branch** del local i del remot i els **tags**:
![](img/Pasted%20image%2020240619175141.png)

Si modifiquem o creem arxius nous, ens apareix un número a damunt de l'icona del pluguin indicant els canvis pendents de ser confirmats i també les lletres `M` (**modified**) i `U` (**untracked**):
![](img/Pasted%20image%2020240619175322.png)

Si despleguem la `command palette` prement <kbd>Control</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> i escrivim `Git` ens apareixen totes les opcions disponibles:

![](img/Pasted%20image%2020240619175842.png)

### Ús de GitHub Copilot
![](img/Pasted%20image%2020240619180811.png)

---

## Integració Obsidian
Obsidian és un **editor de text** pensat per a **prendre notes** i per a publicar articles purament usant sintaxi **Markdown**.

Per a exemple, és útil per a crear la documentació d'aquest curs de formació de Git i GitHub.

Per usar l'integració amb Git, cal anar a la roda de configuració d'abaix a l'esquerra i navegar pels `community plugins`:
![](img/Pasted%20image%2020240619180058.png)

Buscar `Git` i instal·lar-lo:
![](img/Pasted%20image%2020240619180147.png)

Aleshores ja podrem usar la `command palette` apretant <kbd>Control</kbd> + <kbd>P</kbd>:
![](img/Pasted%20image%2020240619180333.png)

