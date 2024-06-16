- **Organitzar les sessions a mode de NCA amb:**
	- **Obertura del que parlarem al llarg de la sessió del dia actual**
	- **Part teòrica uns 20'**
	- **Exemples, demo**
	- **Descans**
	- **Part pràctica**
	- **Tancament**
	- **Comentaris**
- **Fer document de seguiment per tal d'establir quins doc teòrics i quines activitats farem cada dia.**
- **Amb el Chat fer un test de continguts per al contingut de cada dia per tal de tenir 5 qüestonaris amb 5 notes automàtiques?**
- Fer qüestionari de G Forms a cada sessió inici o final
- Comandes a considerar:
	- git stash
- TAXX: crear i usar branques en local
- TAXX: Imprimir plantilles del Git LifeCycle buides i proposar-los exercici on l'hagin de dibuixar l'estat dels fitxers. Fer-ho en vàries etapes del curs, també després d'afegir el gitignore i d'altres comandes que afecten al life cycle del repo. Fer-los fer també algun exercici omplint la plantilla però en draw-io
- TAXX: Crear perfil GitHub
- TAXX: Crear repo remot a GitHub i clonar en local
- TAXX: Fer-los fer una activitat amb MakeCode Microbit i/o MakeCode Arcade
- Crear un repo remot a GitHub i clonar en local i treballar dues persones
- Rebase
- Merge amb conflictes
- Ús del GitHub GUI
- Ús de Visual Studio Code integrat
- Ús de IntelliJ integrat
- Ús de Obsidian integrat
- Conventional commits:
	- **Com generar les release notes automàticament a partir dels conventional commits?**
- Commit ammend?
- Perquè des del terminal de windows no em demana les credencials ni **token** per fer commit al remot?
- GitHub:
	- Navegació
	- GitHub Code Spaces
	- GitHub Tags
	- GitHub Pages: GitHub Releases
	- GitHub Classroom

---

- `git fetch` descarrega els canvis del repositori remot al teu repositori local, però no aplica els canvis directament al teu directori de treball. En lloc d'això, actualitza els "punts d'intercanvi" (o "punts d'ancoratge") locals que fan referència als "commits" del repositori remot.
    
- `git pull`, d'altra banda, fa `git fetch` primer i després aplica els canvis al teu directori de treball. És com una combinació de `git fetch` i `git merge`.

---

El missatge "Your branch is up to date with 'origin/main'" significa que la teva branca local (en aquest cas, `main`) està sincronitzada amb la corresponent branca del repositori remot (també anomenada `main` en aquest cas).

En resum, el missatge vol dir que no hi ha canvis nous en la branca remota que necessitin ser descarregats i aplicats a la teva branca local, i que tampoc hi ha canvis en la teva branca local que necessitin ser pujats al remot. En aquest estat, la teva branca local i la branca remota estan perfectament sincronitzades.

---

El temari a impartir segons el formulari entregat és:
1. Introduïr les bases de la tecnologia de control de versions en el desenvolupament de software anomenada Git des d'un enfoc inicial.
	1. Utilitat
	2. Comandes bàsiques 
	3. Instal·lació
2. Aprendre el funcionament de la plataforma GitHub, líder mundial en el sector de serveis de proveïment de gestió de repositoris remot en el procés de desenvolupament de software.
	1. Markdown
	2. GitHub Gists
	3. GitHub Pages
	4. Comunitat GitHub
3. Usar les eines introduïdes en casos pràctics reals a nivell professional introductori.
	1. Integració amb IDEs (IntelliJ i Visual Studio Code)
4. Aplicacions reals de la tecnologia a l'aula per a CFGS d'Informàtica i Comunicacions
	1. Plataforma educativa MakeCode integrada amb GitHub i Microsoft (microbit i Arcade)
	2. Plataforma educativa GitHub Classroom
---

