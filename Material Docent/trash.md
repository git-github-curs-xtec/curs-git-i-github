### Com Modificar el Comentari d'un Commit de Git

Modificar el comentari d'un commit a Git és una operació que es fa utilitzant la comanda `git commit --amend`. Aquesta comanda permet canviar el missatge de l'últim commit que has fet. Aquí tens una explicació detallada de com fer-ho, així com algunes consideracions importants.

### Ús de `git commit --amend`

#### Pas a Pas per Modificar l'Últim Commit

1. **Assegura't d'Estar a la Branca Correcta**
   Primer, assegura't que estàs a la branca correcta on es troba el commit que vols modificar:
   ```sh
   git checkout nom-de-la-branca
   ```

2. **Modifica el Missatge del Commit**
   Utilitza la comanda `git commit --amend` per editar el missatge del commit:
   ```sh
   git commit --amend
   ```
   Aquesta comanda obrirà el teu editor de text predeterminat amb el missatge de l'últim commit. Pots editar aquest missatge segons sigui necessari. Quan hagis acabat, desa i tanca l'editor.

3. **Pujar els Canvis al Repositori Remot**
   Si ja has pujat l'últim commit al repositori remot, hauràs de forçar l'actualització amb la comanda `git push` per sobreescriure el commit existent:
   ```sh
   git push --force
   ```
   **Nota:** Utilitzar `--force` pot ser perillós perquè pot sobreescriure els canvis en el repositori remot. És important assegurar-te que ningú més està treballant en la mateixa branca abans de forçar l'actualització.

### Exemples

#### Exemple 1: Modificar el Missatge de l'Últim Commit

Suposem que l'últim commit té el missatge "Corregir error menor" i vols canviar-lo a "Correcció d'error en el formulari de registre":

```sh
git commit --amend
```
A l'editor, canvia:
```plaintext
Corregir error menor
```
a
```plaintext
Correcció d'error en el formulari de registre
```
Desa i tanca l'editor. Després, puja els canvis:
```sh
git push --force
```

### Consideracions Importants

- **Historial Compartit**: Evita modificar commits que ja han estat compartits amb altres membres del teu equip, ja que això pot causar conflictes i confusions. Sempre comunica't amb el teu equip abans de fer una operació `--force`.
- **Ús de `rebase` per Modificar Commits Anteriors**: Si necessites modificar el missatge d'un commit que no és l'últim, pots utilitzar `git rebase -i`. Això obrirà una llista interactiva dels commits recents i podràs seleccionar el commit que vols modificar.

### Modificar Commits Anteriors

1. **Inicia un Rebase Interactiu**
   ```sh
   git rebase -i HEAD~n
   ```
   On `n` és el nombre de commits anteriors que vols veure. Aquesta comanda obrirà una llista dels últims `n` commits en el teu editor de text.

2. **Selecciona el Commit per Editar**
   Canvia `pick` per `reword` davant del commit que vols modificar. Per exemple:
   ```plaintext
   reword abc1234 Correcció d'error en el formulari de registre
   pick def5678 Afegir nova funcionalitat
   ```

3. **Modifica el Missatge del Commit**
   Desa i tanca l'editor. Git obrirà un altre editor on podràs modificar el missatge del commit seleccionat.

4. **Completa el Rebase**
   Desa i tanca l'editor després de modificar el missatge. Si no hi ha conflictes, el rebase es completarà automàticament. Si hi ha conflictes, resol-los i continua el rebase:
   ```sh
   git rebase --continue
   ```

5. **Puja els Canvis**
   Igual que abans, hauràs de forçar l'actualització si ja has pujat els commits al repositori remot:
   ```sh
   git push --force
   ```

### Resum

Modificar el comentari d'un commit a Git és senzill amb `git commit --amend` per l'últim commit o `git rebase -i` per commits anteriors. Sempre és important tenir en compte les bones pràctiques per evitar problemes amb l'historial compartit.