# TA04: Git branches

## Enunciat
En aquesta tasca **crearem branques** en el nostre repositori local usant el terminal de Git i en farem el seu fusionat.

0. Si la nostra branca principal no es diu `main`, la renombrarem usant `git branch -M main`.
1. Dins de la branca `main`, hi posarem el fitxer `hello-world.py`, l'afegirem a `stage` i el confirmarem.
	El fitxer té el següent contingut:
	```python
	def hello_world:
	  print("Hello World!")
	
	hello_world()
	```

>[!WARNING]
>Hi ha cap expert en `python` a la sala?? Aquest codi conté errors!!!

2. Ara, dins de la branca `main` crea una branca nova que li direm `bugfix`.
3. Ens mourem a la branca `bugfix` i crearem una branca nova que es dirà: `fix-hello-world` a la mateixa vegada que ens hi movem a dins.
4. Un cop dins de la branca `bugfix/fix-hello-world` solucionarem el problema del fitxer `hello-world.py` i confirmarem els seus canvis.
5. Farem merge entre `bugfix/fix-hello-world` i `bugfix` i en comprovem els resultats
6. Eliminarem la branca `bugfix/fix-hello-world`
7. Farem merge entre `bugfix` i `main` i en comprovem el resultat
8. Eliminarem la branca `bugfix`

---
## EXTRA
Si t'ha semblat molt fàcil, prova-ho ara **provocant un conflicte** de versions al fitxer `hello-world.py` entre les diverses branques i soluciona'l tal i com podem trobar dins del material de teoria.

---
## Entrega
1. Entrega captures de pantalla del terminal on es vegi com has fet el procés.
