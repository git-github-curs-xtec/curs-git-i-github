# Introducció a Git
Per començar, cal saber que **Git** i **GitHub** no són el mateix. Git es tracta d'un software de control de versions i GitHub es tracta d'un proveïdor de hosting de repositoris remots de Git.

Sense Git, GitHub no existiria, per tant, comencem pel principi: tal com hem comentat, **Git** és un programari lliure pensat per a la gestió del control de versions en local durant el desenvolupament d'un software.
Se centra en l'eficiència i confiabilitat de manteniment de versions d'aplicacions amb una enorme quantitat de fitxers de codi font.

Va ser creat el 2005 per [**Linus Torvalds**](https://ca.wikipedia.org/wiki/Linus_Torvalds) *(28 de Desembre de 1969)* mentre desenvolupava el kernel de Linux el qual va batejar sota el seu propi nom. 

![Linus Trovalds](https://upload.wikimedia.org/wikipedia/commons/thumb/0/01/LinuxCon_Europe_Linus_Torvalds_03_%28cropped%29.jpg/215px-LinuxCon_Europe_Linus_Torvalds_03_%28cropped%29.jpg)

Segons Linus, el nom de **'Git'** prové del terme britànic *git* que en argot significa *"persona desagradable"* i en les seves pròpies paraules, va dir: 

> *"Sóc un bastard egoista, i anomeno tots els meus projectes amb el meu nom. Primer 'Linux', ara 'Git'"*

Oficialment es va presentar el [7 d'Abril de 2005](https://ca.wikipedia.org/wiki/Git) sota la llicència [GNU GPL](https://ca.wikipedia.org/wiki/GNU_General_Public_License) de la [Free Software Foundation](https://ca.wikipedia.org/wiki/Free_Software_Foundation) creada per [Richard Stallman](https://ca.wikipedia.org/wiki/Richard_Matthew_Stallman) *(16 de Març de 1953)*

![Richard Stallman](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3d/Richard_Stallman_at_Pittsburgh_University.jpg/300px-Richard_Stallman_at_Pittsburgh_University.jpg)

El seu principal **valor afegit** és que guarda un registre amb data, hora i usuari responsable de tots els canvis que es facin en els fitxers dins d'un determinat directori. És com si tinguèssim un auditor que està constantment vigilant i registrant totes les modificacions que es facin en els fitxers així com els nous fitxers creats i els esborrats. 

Tot i que Git va ser incialment creat per al control de canvis en codi font durant el desenvolupament de software, és a dir, per a monitoritzar fitxers de text pla; també és capaç de fer tracking de diversos tipus de fitxer en escenaris diferents al desenvolupament de software. Ara bé, no és adeqüat per al control de fitxers binaris com per exemple els *.docx*

L'ús de Git no serà útil doncs per a la gestió, creació i edició de fixers tipus office.

L'alternativa rudimentària a l'ús del Git durant el desenvolupament de programari, és anar guardant versions del codi manualment creant còpies dels arxius que funcionen a mode check-point afegint-los vxx al final del nom del fitxer abans de ser modificats amb les noves implementacions.

Per si sol, aquest mètode pot ser causant d'errors, de pèrdua de parts del codi, difícil de controlar els canvis aplicats, molt complicat de desfer un canvi concret i si ens posem en l'**escenari de desenvolupament de software col·laboratiu** amb un equip de persones, ja es converteix en una tasca molt laboriosa: 
- La meva versió v23 del codi conté el mateix que la versió v22 de l'Anna més els meus últims canvis?
- Què passa si mentre jo desenvolupo una funcionalitat sobre la versió 17 del fitxer, el Joan també està desenvolupant una altra funcionalitat sobre la mateixa versió 17 del codi i acaba abans que jo? He d'agafar aquesta nova versió i aplicar-hi els meus canvis al damunt? I si, mentre ho faig, la Maria aplica un canvi d'estil sobre el codi que acaba de fer en Joan? He d'esperar-me que ella acabi primer?
- Quina és la meva versió de codi doncs?
- Estic segur/a que tinc tot el codi dels meus companyis i que no perdrem res quan jo apliqui els meus canvis?
- etc.

> [!WARNING]
> Sense fer ús de cap eina de control de versions, com **desenvoluparieu un software col·laborativament?**

---
# Funcionament de Git
A partir del moment en què iniciem un **repositori de Git** dins d'una carpeta del nostre disc dur, el programa farà seguiment de tots els canvis que es facin dins dels fitxers ja existents així com també guardarà un registre dels arxius eliminats i de tots els arxius nous creats.

> [!IMPORTANT]
>  **Repositori de Git:** Un repositori és l'element més bàsic de Git i és l'espai on podem emmagatzemar arxius de codi i l'historial de revisió de cadascun d'ells. Els *repo* poden tenir múltiples col·laboradors, ser públics o privats, ser locals o remots.

Per a fer aquest seguiment, Git guarda múltiples *"instantànies"* de l'estat de tots els arxius continguts dins d'aquella carpeta on hem iniciat el repositori i les diferències entre *captura* i *captura*.

Les captures, acostumen a ser fetes pels usuaris desenvolupadors de forma asíncrona; és a dir, quan han acabat una part del codi, una funcionalitat, han resolt una incidència, etc.

Si hem jugat al Sonic de la Sega, al Super Mario Bros o a qualsevol altre videojoc de plataformes, podem pensar que, cada instantània del codi, és com un *checkpoint*, punt a partir del qual, si el nostre personatge cau i mor, tornarem allà i no a l'inci de la pantalla.

![Sonic](http://www.starquail.com/michael/sonic/clear.gif)

Es tracta d'anar fent versions dels fitxers a mesura que anem validant noves parts del desenvolupament.



