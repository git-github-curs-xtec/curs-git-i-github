# Git conventional commits
### Què són els Conventional Commits?

Els **Conventional Commits** són una convenció per a redactar **missatges de commit clars** i descriptius **seguint** un **format estàndard**. Aquesta convenció ajuda a millorar la llegibilitat de l'historial de commits i a **automatitzar la generació de versions** *(versioning)* i **notes de publicació** *(release notes)* de l'aplicació.

### Format Bàsic d'un Conventional Commit

El format general és:

```
<tipus>(<àmbit opcional>): <resum curt>

[cos opcional]

[peu opcional]
```

### Tipus de Commits

Els tipus de commits més comuns són:

- **feat**: Afegir una nova funcionalitat.
- **fix**: Corregir un error.
- **docs**: Canvis a la documentació.
- **style**: Canvis que no afecten el significat del codi (espais, format, punts i comes, etc.).
- **refactor**: Canvis en el codi que no corregeixen errors ni afegeixen funcionalitats (millores de rendiment, etc.).
- **test**: Afegir o corregir tests.
- **chore**: Canvis al procés de construcció o eines auxiliars i llibreries com ara documentació de generació.

### Exemples de Conventional Commits

#### 1. Afegir una Nova Funcionalitat

```plaintext
feat: afegir autenticació d'usuari

- Implementar login
- Afegir validació de contrasenya
- Crear pàgina de registre
```

#### 2. Corregir un Error

```plaintext
fix: corregir error de navegació en la pàgina principal

- Resoldre problema de bucles infinits
- Actualitzar tests relacionats
```

#### 3. Canvis en la Documentació

```plaintext
docs: afegir documentació per a la nova API d'autenticació

- Documentar endpoints de login i registre
- Afegir exemples d'ús
```

#### 4. Canvis de Format

```plaintext
style: formatar arxius segons la guia de codificació

- Ajustar indentació a 4 espais
- Afegir espais en blanc entre funcions
```

#### 5. Refactorització del Codi

```plaintext
refactor: reestructurar el mòdul d'autenticació

- Separar la lògica de negoci en un servei apartat
- Millorar la llegibilitat del codi
```

#### 6. Afegir Tests

```plaintext
test: afegir tests unitàris per al mòdul d'autenticació

- Cobrir tots els casos d'ús del login
- Afegir tests per a la validació de contrasenya
```

#### 7. Tasques de Manteniment

```plaintext
chore: actualitzar dependències del projecte

- Actualitzar a la darrera versió de React
- Actualitzar llibreries de testing
```

### Cos i Peu Opcional

El cos del commit proporciona més detalls sobre els canvis i es col·loca després d'una línia en blanc seguint el resum curt. El peu opcional pot incloure informació com ara els números d'incidència.

#### Exemple Complet Amb Cos i Peu

```plaintext
feat: afegir funcionalitat de recuperació de contrasenya

- Crear formulari de recuperació de contrasenya
- Afegir enviament de correu electrònic amb l'enllaç de recuperació
- Implementar validació de token

Closes #123
```

### Beneficis dels Conventional Commits

1. **Claredat**: Els missatges de commit són més fàcils de llegir i entendre.
2. **Automatització**: Facilita la generació automàtica de versions i notes de publicació.
3. **Estandardització**: Tots els desenvolupadors segueixen el mateix format, la qual cosa millora la consistència del projecte.

### Implementació en el Teu Flux de Treball

1. **Establir una Convenció**: Decidir amb l'equip quins tipus de commits utilitzar i com descriure'ls.
2. **Integració**: Utilitzar eines com `commitizen` per ajudar els desenvolupadors a seguir aquesta convenció.
3. **Automatització**: Utilitzar eines com `semantic-release` per automatitzar el versioning i la generació de notes de publicació basades en els commits.

### Eines Recomanades

- **Commitizen**: Una eina que ajuda a redactar missatges de commit seguint el format Conventional Commits.
  ```sh
  npm install -g commitizen
  ```

- **Semantic Release**: Automatitza el procés de llançament basat en els commits.
  ```sh
  npm install -g semantic-release
  ```
---

>[!TIP]
>Per més info, veure [conventionalcommits.com](https://www.conventionalcommits.org/en/v1.0.0/)

