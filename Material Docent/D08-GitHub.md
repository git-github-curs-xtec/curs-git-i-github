# GitHub
Fins ara hem vist com desenvolupar programari amb suport de repositori local usant Git; ara anirem més enllà amb el suport de **[GitHub](https://github.com/)** per als repos remots.

**GitHub** és actualment la plataforma líder mundial del sector en quant al suport i hosting de repositoris remots.

Va ser fundat a Califòrnia (USA) el 8 de Febrer de 2008 i compta actualment amb més de 100 milions d'usuaris arreu del món.

El Juny de 2018 GitHub va llançar **GitHub Education** oferint entorns educacionals per a les escoles.

Microsoft va comprar GitHub el 26 d'Octubre de 2018 i donant-li encara més impuls per davant de **GitLab**, **Bitbucket** and **SourceForge**.

El seu logotip és el reconegut [**Octocat**](https://octodex.github.com/):
![Octocat](https://octodex.github.com/images/original.png)
## Funcionalitats de GitHub
D'entrada ens proveeix de l'última etapa del cicle de vida de Git de forma gratuïta: el **repositori remot**.

Aquest no és un fet trivial, ja que ens permet **desenvolupar software col·laborativament** amb un suport de versionat per darrera.

Seria l'equivalent a escriure un document word o un excel col·laborativament usant les eines de Google Drive o de Microsoft Office 365, però amb múltiples documents dins de la mateixa carpeta i auditant els canvis de tots els usuaris sobre tots els documents al mateix temps.

Aquest servei ens permet una millor organització i minimitzar el risc perdre parts del nostre codi.

## Donar-se d'alta a GitHub
Crear un compte a GitHub és molt fàcil i gratuït, només cal anar al seu portal https://github.com/:

![[Pasted image 20240616114210.png]]

I escollim **Sign Up**:
![[Pasted image 20240616114255.png]]

>[!NOTE]
>Amb un **correu electrònic** d'un **domini d'educació** com per exemple del nostre institut o el de @xtec, podem acollir-nos als beneficis de **[GitHub Education](https://github.com/edu/students)** que incorpora tots els múltiples avantatges de **GitHub Pro** tals com *[GitHub Copilot](https://github.com/features/copilot)* gratuït.

## Personalitzar el nostre perfil

### Accions bàsiques
És interessant crear un perfil de caire professional amb l'interès de que es converteixi en el portafoli dels nostres projectes.

En el sector professional de la informàtica, es valora molt més un **portfoli digital de projectes** que no pas un currículum que diu que dominem 18 llenguatges de programació diferents.

Podem cutomitzar el nostre perfil fàcilment afegint-t'hi:
- Una foto de perfil
- Una petita biografia personal
- Els pronoms amb els quals ens sentim indentificats/des *(si s'escau)*
- Configuració de la ubicació i zona horària per si treballem en projectes internacionals
- Link amb els perfils de xarxes socials
- El nostre estat
- Altres...

>[!TIP]
>Aquí trobarem la documentació oficial sobre com configurar el nostre perfil públic de GitHub: [link](https://docs.github.com/es/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/personalizing-your-profile)

### Administrar el README del perfil
om que som desenvolupadors/es professionals, també crearem el **README**.md del nostre pefil. 

Per a fer-ho, farem:
1. **Crear un repositori públic** que es **digui igual** que el **nom** del nostre **usuari** de **GitHub**
2. Crearem i afegirem un **fitxer anomenat README.md** dins del repositori
3. Editarem el contingut del fitxer usant **Markdown** per tal de donar-li **contingut** i **format**

Això ens farà que a la pàgina principal del nostre perfil se'ns mostri un contingut de forma personalitzada.

>[!TIP]
>Aquí trobarem la **documentació oficial** sobre com crear el **README** del nostre perfil: [link](https://docs.github.com/es/account-and-profile/setting-up-and-managing-your-github-profile/customizing-your-profile/managing-your-profile-readme)

#### Exemple:
![[Pasted image 20240616123639.png]]


# Crear un token personal
Per tal de poder **usar GitHub** com a plataforma de suport pels repositoris remots des del **terminal**, haurem de passar a través de la seva **API**.

Per a poder-ho fer, necessitarem **crear un token personal** que usarem des del terminal com a **password** conjuntament **amb** el nostre nom d'**usuari de GitHub**.

Anirem a la part superior dreta i sel·leccionarem <kbd>Settings</kbd>:
![[Pasted image 20240616124419.png]]
Anirem a **<kbd>Developer settings</kbd****>:
![[Pasted image 20240616124524.png]]

Generarem un **new token (classic)**:
![[Pasted image 20240616124808.png]]

Escollirem les següents **blocs** d'opcions de **permisos**:
- **repo**
- **workflow**
- **gist**
- **notifications**
- **user**
- **codespace**
- **copilot**
- **project**

>[!NOTE]
>Podem escollir per quant de **temps** serà **vigent**.
>Quan expiri, n'haurem de crear un de nou.

![[Pasted image 20240616125145.png]]

![[Pasted image 20240616125043.png]]


**Generem token** i ens donarà un codi similar a aquest: `ghp_mvoK09jll9ehQFFW2SciAxv2pY2Jxq3xFrOK`

>[!WARNING]
>**Copieu el codi** i **guardeu-lo** a algun lloc segur perquè **no es tornarà a mostrar** mai més quan sortiu d'aquesta pantalla.
>![[Pasted image 20240616125504.png]]

Aquest codi l'usarem quan ens demani el password des del terminal en les accions de `git push`

****
# Annex
Com a curiositat, i per a tancar el cercle de Git -> GitHub, aquí tenim el **repositori** del **kernel de Linux** de **Linus Torvalds**: https://github.com/torvalds/linux.



---
- git pull
