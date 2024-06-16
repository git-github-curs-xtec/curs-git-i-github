# Visors GUI de Git
Ara hem vist com crear gestionar un repo local usant el terminal del sistema operatiu, crear branques, usar `.gitignore`, etc.

Però també estar bé conèixer que hi ha un conjunt d'eines que permeten navegar els repositoris usant interfícies gràfiques i poder veure així la **representació gràfica** de les diferents etapes del **cicle de vida de Git**, els diferents canvis en el contingut dels fitxers al llarg de les diferents versions de l'històric de commits, les seves **branques** representades sobre una línia temporal, etc.

Depèn de cada sistema operatiu *(MacOS, Windows OS, LInux OS)* n'hi ha de diferents i amb diferent tipus de llicència.

Un dels més coneguts per Windows i MacOS és el **[GitHub Desktop](https://desktop.github.com/)** i tot i que hi ha [maneres d'instal·lar-lo a Ubuntu](https://github.com/shiftkey/desktop?tab=readme-ov-file#installation-via-package-manager), encara no està disponible al repositori de software tradicional.

![GitHub Desktop](https://github.blog/wp-content/uploads/2021/03/multiple-commits.gif)

>[!TIP] Instal·lar GitHub Desktop a Ubuntu 22.x
>https://www.youtube.com/watch?v=ki0MuWceGk4&ab_channel=ZacsTech
>

Per aquest curs usarem el **[GUI Git Cola](https://git-cola.github.io/index.html)** que no és el més bonic dels existents però està disponible dins de la bossa de software estàndard dels repos d'Ubuntu i és de [llicència GNU](https://git-cola.github.io/license.html) i està desenvolupat usant la pròpia tecnologia de Git.

Permet visualitzar el mateix contingut que ens dona `git status` però en format gràfic:
![Git Cola status](https://git-cola.github.io/images/screenshot-main-linux.png)

A través de l'eina Git DAG, ens permet visualitzar les branques que tenim en el nostre repositori:
![Git DAG](https://git-cola.github.io/images/dag.png)

També ens permet resoldre conflictes usant un editor de text tal com **Gedit** que ja ve integrat dins de Gnome o de **Gnome Nano** pels més *old school*