# Git ignore
### Què és `.gitignore`?

El fitxer `.gitignore` és un fitxer de text pla i ocult en un repositori de Git que especifica quins fitxers i directoris han de ser ignorats per Git. Quan es fa un commit, Git omet els fitxers i directoris especificats en el fitxer `.gitignore`, evitant que siguin inclosos en el seguiment de canvis del repositori.

### Ús de `.gitignore`

1. **Evitar arxius temporals**: Fitxers generats per l'IDE, compiladors, o altres eines que no han de ser versionats.
2. **Mantenir la seguretat**: Fitxers que contenen informació sensible com contrasenyes o claus API.
3. **Millorar la neteja del repositori**: Evitar que fitxers innecessaris o temporals es barregin amb el codi font.

### Exemple de fitxer `.gitignore`

Un exemple de fitxer `.gitignore` podria ser:

```plaintext
# Ignora els fitxers de compilació
*.class
*.o
*.so
*.dll
*.exe

# Ignora els fitxers temporals del sistema operatiu
.DS_Store
Thumbs.db

# Ignora els fitxers de l'IDE
.idea/
*.iml
*.swp

# Ignora les carpetes de depuració
node_modules/
target/
build/

# Ignora els fitxers de configuració personal
*.log
*.env
.vscode/

# Ignora els fitxers de seguretat
secrets.yml
credentials.json
```

### Crear i Utilitzar `.gitignore`

1. **Crear el fitxer `.gitignore`**:
   - Al directori arrel del teu repositori, crea un fitxer anomenat `.gitignore`.

2. **Afegir regles al fitxer `.gitignore`**:
   - Obre el fitxer `.gitignore` amb un editor de text i afegeix les regles que especifiquen els fitxers i directoris a ignorar. Podem especificar noms d'arxiu concret en literal o establir patrons de tipus de fitxer que volem que s'ignorin (típicament es fa per extensió de fitxer i usant patrons igual que fariem per buscar arxius dins d'un explorador de fitxers).

3. **Aplicar el fitxer `.gitignore`**:
   - Després d'afegir les regles, guarda el fitxer `.gitignore`.
   - Si ja hi ha fitxers que compleixen les regles del `.gitignore` però han estat prèviament versionats, els has de treure de l'índex amb la comanda següent per tal de que Git deixi de seguir-los:
     ```sh
     git rm --cached nom_del_fitxer
     ```
   - Fes un commit del fitxer `.gitignore`:
     ```sh
     git add .gitignore
     git commit -m "Afegir fitxer .gitignore"
     ```

### Exemple Pràctic

Suposem que tens un projecte JavaScript i no vols versionar els fitxers `node_modules/`, els fitxers de logs i els fitxers de configuració de l'IDE.

1. Crear un fitxer `.gitignore` a l'arrel del projecte.
2. Afegir les regles següents al `.gitignore`:

   ```plaintext
   # Ignora els paquets instal·lats
   node_modules/

   # Ignora els fitxers de log
   *.log

   # Ignora els fitxers de configuració de l'IDE
   .vscode/
   ```

Amb aquest fitxer `.gitignore`, Git ignorarà la carpeta `node_modules/`, qualsevol fitxer amb extensió `.log` i la carpeta `.vscode/`.

Això ajuda a mantenir el repositori net i centrat en el codi font i els fitxers que són realment importants per al projecte.

---

### Regles avançades de `.gitignore`
Suposem que volem excloure tot un directori del versionat de Git, però hi ha un únic fitxer d'aquell carpeta pel qual sí que en volem fer control de versions i no el volem canviar d'ubicació.

Per a aquests casos, podem usar l'**operador de negació** `!` 

### Exemples Avançats d'Ús de `.gitignore` amb Negacions

#### 1. Ignorar un Directori Enter Però Incloure Alguns Fitxers

Suposem que tens un directori `logs/` on vols ignorar tots els fitxers excepte els fitxers `.keep`.

```plaintext
# Ignora tots els fitxers del directori logs/
logs/*

# Però inclou els fitxers .keep
!logs/*.keep
```

#### 2. Ignorar Tots els Fitxers d'un Tipus Excepte un de Concret

Si vols ignorar tots els fitxers `.log` excepte `error.log`:

```plaintext
# Ignora tots els fitxers .log
*.log

# Però inclou error.log
!error.log
```

#### 3. Ignorar Tots els Fitxers en un Directori Determinat Exceptuant-ne Alguns

Si tens un directori `config/` on vols ignorar tots els fitxers excepte `config.yml` i `config.production.yml`:

```plaintext
# Ignora tots els fitxers del directori config/
config/*

# Però inclou config.yml i config.production.yml
!config/config.yml
!config/config.production.yml
```

#### 4. Negacions Amb Patrons Més Complexos

Pots utilitzar negacions amb patrons més complexos. Suposem que vols ignorar tots els fitxers en el directori `dist/` excepte els fitxers `.min.js`:

```plaintext
# Ignora tots els fitxers en dist/
dist/**

# Però inclou tots els fitxers .min.js en qualsevol subdirectori de dist/
!dist/**/*.min.js
```

### Exemple Complet de `.gitignore`

```plaintext
# Ignora els fitxers de compilació
*.class
*.o
*.so
*.dll
*.exe

# Ignora els fitxers temporals del sistema operatiu
.DS_Store
Thumbs.db

# Ignora els fitxers de l'IDE
.idea/
*.iml
*.swp

# Ignora les carpetes de depuració
node_modules/
target/
build/

# Ignora els fitxers de configuració personal
*.log
*.env
.vscode/

# Ignora els fitxers de seguretat
secrets.yml
credentials.json

# Ignora tots els fitxers en logs/ però inclou .keep
logs/*
!logs/*.keep

# Ignora tots els fitxers .log excepte error.log
*.log
!error.log

# Ignora tots els fitxers en config/ però inclou config.yml i config.production.yml
config/*
!config/config.yml
!config/config.production.yml

# Ignora tots els fitxers en dist/ però inclou tots els fitxers .min.js en qualsevol subdirectori de dist/
dist/**
!dist/**/*.min.js
```
