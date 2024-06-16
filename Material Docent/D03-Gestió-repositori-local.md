# Comandes d'ús diari
Ara que ja sabem crear un repo local, podem explorar una mica més les seves funcionalitats en diverses situacions.

## Eliminar un arxiu del repo
Per a eliminar físicament un arxiu del repositori, el procediment adeqüat seria usar la comanda de git `git rm nom-fitxer` per tal d'esborrar-lo seguint el cicle de vida de Git.

Un cop esborrat, hem de confirmar els canvis usant `git commit -m "missatge"`.
No cal afegir el canvi a la zona de `staging` perquè l'acció de `git rm` ja ho fa de forma implícita.

D'aquesta manera ens assegurem que l'eliminació del fitxer es fa de forma segura i el podríem recuperar navegant a un commit anterior.

## Recuperar versió confirmada d'un arxiu
En el cas de que tinguem un arxiu amb modificacions actives al *working directory* i ens volguem descartar i tornar a recuperar el fitxer a l'última versió confirmada, podem usar `git checkout nom-fitxer`

**Exemple**:
![[Pasted image 20240614124445.png]]

## Treure un arxiu o carpeta de la staging area
>[!TIP]
>Per a treure un arxiu o carpeta que hem afegit erròniament a la *staging area* i tornar-lo al *working directory* podem usar:
>```bash
>git reset nom-fitxer

>[!TIP]
>També podem usar:
>```bash
>git restore --staged nom-fitxer
>```

**Exemple**
![[Pasted image 20240606192855.png]]

>[!TIP]
>Tot i que en alguna documentació ho desaconsella, també podem usar el punt '.' per a desfer tots els canvis de la *staging area*:
>```bash
>git reset .

## Visualitzar repo en un status anterior
>[!TIP]
>Per a navegar l'estat del codi del repositori segons un commit anterior, podem usar:
>```bash
>git checkout codi

**Exemple:**
![[Pasted image 20240606194312.png]]

Ara Git ens mostra l'estat del repositori segons un commit anterior per a navegar pel seu codi i els seus fitxers com si estiguèssin en un commit previ.
![[Pasted image 20240606194554.png]]

Fixem-nos que el text blau *(main)* ara hi apareix el codi del commit del qual estem veient l'estat del repositori.

>[!TIP]
>Podem desfer aquesta pre-visualització usant:
>```bash
>git switch -
>```
 
 **Exemple**
 ![[Pasted image 20240606194744.png]]

## Tornar el repo a un punt anterior
>[!TIP]
>Per a moure el repositori a un status anterior, hem de localitzar el codi únic del commit i usar el **reset**:
>```bash
>git reset --hard codi

**Exemple:**
![[Pasted image 20240606193359.png]]

L'arxiu *adeu.txt* s'ha eliminat del repositori i també físicament del directori. Aquest arxiu ara ja no es pot recuperar.

---
## Exemple complet

Tenim una carpeta anomenada **curs-git** on hi hem iniciat un repositori de Git en local.

Hi hem fet les següents modificacions de contingut dins del working directory:
1. Hem creat l'arxiu **hola.txt** amb cert contingut textual
2. Hem fet un **git add hola.txt**
3. Hem fet un **git commit hola.txt -m "chore: afegir hola.txt**" i ens ha generat el commit amb codi **9c5c69c**
4. Hem creat l'arxiu **adeu.txt** amb cert contingut textual
5. Hem fet un **git add adeu.txt**
6. Hem fet un **git commit adeu.txt -m "chore: afegir adeu.txt**" i ens ha generat el commit amb codi **e040a4d**
7. Hem creat l'arxiu **missatge.txt**  amb cert contingut textual
8. Hem creat l'arxiu **contingut.md** amb cert contingut textual
9. Manualment hem eliminat l'arxiu **adeu.txt*** del working directory
10. Hem fet un **git add contingut.md**

Des del terminal veiem això:
![[Pasted image 20240608203954.png]]

### El repositori es mostra així
![[GitRepoStatus.png]]

>[!TIP]
>Per a entendre millor el life cycle de Git, podem entendre el *working directory* com el que nosaltres veiem dins de la carpeta de nostre ordinador on hem desplegat el repositori local.

Després de les accions fetes, l'estat actual del life cycle del repositori **curs-git** és:
1. L'arxiu **hola.txt** es troba dins del *working directory* amb el mateix contingut que el que tenim a la zona confirmada al seu últim commit e040a4d.
2. L'arxiu **adeu.txt** ha estat esborrat i ja no és present físicament dins del directori on tenim el repositori desplegat. Però sí que hi ha una còpia oculta del seu contingut dins del sistema de versionat de Git per si el volguèssim recuperar en el futur. Ara mateix es troba a la *staging area* pendent de confirmat la seva eliminació i també es troba present dins de la zona confirmada ja que formava part de l'últim commit fet.
3. L'arxiu **contingut.md** és de nova creació i encara no li hem fet cap commit però sí que el tenim a la *staging area pendent de ser confirmat*.
4. L'arxiu **missatge.txt** es troba dins del *working directory* però no s'ha afegit dins del control de versionat del repository; per tant, Git no n'està fent seguiment ni de la seva creació ni del versionat del seu contingut. Això pot ser útil quan tinguem arxius dins de la carpeta del *working directory* pels quals no volem que se'n faci seguiment. Per exemple, per l'enunciat d'un exercici, per unes notes personals, per un llistat de coses pendents de fer, per a dades sensibles, etc.