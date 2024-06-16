# Git rebase
### Què és `git rebase`?

La comanda `git rebase` és una **eina de Git** que **permet modificar i reescriure l'historial de commits**.

El rebase es pot utilitzar per a:
1. **Modificar el comentari** de qualsevol commit
2. **Combinar commits** d'una branca a una altra de manera lineal enlloc d'usar `git merge`.
3. **Eliminar commits** del log de l'historial de canvis.
4. **Modificar el contingut** d'un commit anterior.
5. **Modificar l'ordre dels commits** dins de l'historial.
6. ...

### Com Fer un Rebase en Git ?

Hi ha dues formes principals d'utilitzar `git rebase`:

1. **Rebase Local**: Per actualitzar la branca local amb els canvis d'una altra branca.
2. **Rebase Interactiu**: Per reescriure l'historial de commits, permetent-te editar, combinar, o eliminar commits.

#### 1. Rebase Local

Aquesta forma de rebase aplica els commits de la branca actual sobre una altra branca.
En lloc d'utilitzar `git merge`, que crea un commit de fusió, `git rebase` aplica els canvis de la branca actual sobre una altra branca com si fossin nous commits.

```sh
git switch feature/nova-funcionalitat
git rebase main
```

##### Exemple d'ús de rebase local
1. **Crear una Branca Nova**:
   ```sh
   git switch -c feature/nova-funcionalitat
   ```

2. **Fer Canvis i Commits**:
   ```sh
   # Fer canvis en el codi
   git add .
   git commit -m "feat: afegir nova funcionalitat"
   ```

3. **Rebase sobre la Branca Principal**:
   ```sh
   git switch main
   git pull origin main  # Assegura que la branca principal està actualitzada
   git switch feature/nova-funcionalitat
   git rebase main
   ```

4. **Resoldre Conflictes (si n'hi ha)**:
   - Editar fitxers conflictius amb un editor de text eliminant les marques d'inici i final de branca de cada línia de conflicte.
   - Continuar el rebase.
     ```sh
     git add fitxer-resolt
     git rebase --continue
     ```

5. **Pujar els Canvis**:
   ```sh
   git switch main
   git merge feature/nova-funcionalitat
   git push origin main
   ```


#### 2. Rebase Interactiu

Ja hem vist anteriorment **com modificar el comentari de l'últim commit fet** en el cas de que ens haguem equivocat usant la comanda `git commit --amend`.

Però en el cas de que volguem **modificar el comentari de múltiples commits antics**, podem usar la comanda `git rebase`  amb el paràmetre `-i` *(rebase interactiu)* per a tal efecte.

```sh
git rebase -i HEAD~n
```

On `n` és el nombre de commits anteriors que vols editar. Això obre l'editor de text per defecte configurat en el sistema operatiu on pots decidir què fer amb cada commit.

#### Exemples d'ús d'un rebase interactiu

1. **Editar l'Historial de Commits**:
   L'editor de text s'obrirà amb un llistat dels últims `n` commits. Pots decidir què fer amb cadascun d'ells:
   - `pick` per deixar el commit sense modificar tal i com està a l'historial *(opció per defecte)*
   - `reword` per tal d'editar el comentari del commit
   - `edit` per modificar el commit sel·leccionat. És a dir, els fitxers i els canvis de codi dels quals fa commit.
   - `squash` per a combinar els canvis del commit actual amb els del commit immediatament anterior, mantenint el missatge del commit actual dins del commit resultant
   - `fixup` per a combinar els canvis del commit actual amb els del commit immediatament anterior, descartant el missatge del commit actual dins del commit resultant
   - `drop` per a eliminar un commit de l'historial

3. **Desar i Tancar l'Editor**:
   Després de fer els canvis desitjats, desa i tanca l'editor.

4. **Continuar el Rebase**:
   Si has triat `edit`, fes els canvis necessaris i després:
   ```sh
   git add .
   git commit --amend
   git rebase --continue
   ```

5. Si volem **combinar commits** podem usar les paraules clau `reword`, `fixup` i `squash`.
   Per exemple, si executem:
   ```sh
   git rebase -i HEAD~7
   ```

I editem l'historial de commits així:
```sh
pick abc123: fix: Correcció error de tipografia
pick def456: feat: Afegir nova funcionalitat
fixup ghi789: fix: Corregir error de codi
pick zzd257: feat: Afegir nova funcionalitat 2
pick hha457: feat: Afegir nova funcionalitat 1
squash ggt123: docs: Afegir documentació
pick eha457: feat: Afegir nova funcionalitat 0

```

El resultat després de combinar els commits serà:
```sh
abc123: fix: Correcció error de tipografia
def456: feat: Afegir nova funcionalitat
zzd257: feat: Afegir nova funcionalitat 2
hha457: feat: Afegir nova funcionalitat 1 docs: Afegir documentació
eha457: feat: Afegir nova funcionalitat 0
```

Ja que el commit `ggt123` s'ha combinat amb `hha457`, conservant el missatge de `hha457` i afegint el missatge de `ggt123` com una nova línia al missatge combinat i el commit `ghi789` s'ha combinat amb el commit `def456` perdent el seu comentari.

Un cop fet haurem d'executar les següents comandes:
   ```sh
   git add .
   git commit --amend
   git rebase --continue
   ```

---

### Resum

`git rebase` és una eina poderosa per mantenir un historial de commits net i organitzat. A més de simplificar la història del projecte, facilita la integració de canvis entre branques, permetent una col·laboració més fluida.

### Consells Pràctics

- **Fer una Còpia de Seguretat**: Abans de fer un rebase important, és una bona pràctica fer una còpia de seguretat de la branca actual.
- **No Rebasejar Branca Compartida**: Evita fer rebase en branques que ja has compartit amb altres desenvolupadors per evitar problemes d'historial inconsistents.
- **Ús Combinat amb `git stash`**: Si tens canvis no confirmats, pots utilitzar `git stash` per desar-los temporalment abans de fer el rebase i després restaurar-los.


---
git push --force
