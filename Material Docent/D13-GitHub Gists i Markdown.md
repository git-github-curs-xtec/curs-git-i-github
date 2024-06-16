### GitHub Gists

#### Què són els GitHub Gists?

GitHub Gists és una característica de GitHub que permet compartir fragments de codi, notes, scripts, i altres tipus d'informació en forma de fitxers únics o col·leccions de fitxers. Els Gists es poden veure com a repositoris simplificats, ideals per a compartir petits projectes o informació d'una manera senzilla i ràpida.

#### Tipus de Gists:
- **Public:** Visibles per a tothom. Qualsevol persona pot veure, clonar, o forjar els Gists públics.
- **Secret:** No apareixen en cerques públiques ni en el perfil de l'usuari, però qualsevol persona amb l'enllaç pot veure'ls i compartir-los.

#### Funcions i Ús:
- **Compartir codi ràpidament:** Ideal per a compartir fragments de codi amb col·laboradors o per a ús públic.
- **Versió i Historial:** Com amb els repositoris complets, els Gists tenen versions, permetent als usuaris veure canvis al llarg del temps.
- **Interacció i Comentaris:** Altres usuaris poden comentar els Gists, facilitant la col·laboració i la discussió.
- **Markdown:** Els Gists suporten Markdown, permetent la creació de documentació amb format.

---
### Markdown

#### Què és Markdown?

Markdown és un llenguatge de marques lleuger creat per convertir text pla en HTML de manera senzilla. S'usa àmpliament per la seva simplicitat i llegibilitat tant en format text pla com en format HTML.

#### Característiques Principals:
- **Senzillesa:** Es pot escriure ràpidament i és fàcil de llegir fins i tot en el format original.
- **Compatibilitat:** Es pot convertir fàcilment a HTML, PDF, i altres formats.
- **Versatilitat:** Utilitzat per documentació, blogs, fòrums, i aplicacions de notes.

#### Sintaxi Bàsica:
- **Encapçalaments:** Utilitzant `#` per definir nivells d'encapçalament.
  ```markdown
  # Encapçalament 1
  ## Encapçalament 2
  ### Encapçalament 3
  ```

- **Text en negreta i cursiva:**
  ```markdown
  *Cursiva* o _Cursiva_
  **Negreta** o __Negreta__
  ```

- **Llistes:**
  ```markdown
  - Element de llista
  - Un altre element
  
  1. Primer element
  2. Segon element
  ```

- **Enllaços:**
  ```markdown
  [Text de l'enllaç](https://www.example.com)
  ```

- **Imatges:**
  ```markdown
  ![Alt text](https://www.example.com/image.jpg)
  ```

- **Codi:**
  - **Inline:**
    ```markdown
    Això és `codi inline`.
    ```
  - **Blocs de codi:**
    ```markdown
    ```python
    def func():
        return "Hello, World!"
    ```
- **Cites:**
  ```markdown
  > Aquesta és una cita.
  ```

#### Ús Combinat amb Gists:

Quan es creen Gists, sovint s'utilitza Markdown per documentar el codi o per explicar la seva funcionalitat. Per exemple, un Gist pot incloure un fitxer de codi Python juntament amb un fitxer README en Markdown que descrigui com utilitzar el codi.

#### Exemple de Gist amb Markdown:
```markdown
# Exemple de Gist

Aquest Gist conté un fragment de codi en Python que imprimeix "Hello, World!".

```python
def hello_world():
    print("Hello, World!")
```

---

>[!TIP]
>Pots navegar per aquest exemple d'un gist: https://gist.github.com/raimonizard/d74052afa8ef785365a03552f98b6d1c
