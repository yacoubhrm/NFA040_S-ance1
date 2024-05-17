------------------------------------------------------------------------------------------------------
INSTALLATION DE VOTRE ENVIRONNEMENT DE TRAVAIL NFA040
------------------------------------------------------------------------------------------------------
Quelles sont les notions qui vont être abordées au cours de cet atelier ?
Cet atelier a pour objectif de vous apprendre à mettre en place place votre environnement de travail dans le cadre de module NFA040. 
Vous allez créer votre hébergement de site, découvrir les Actions et les Secrets GitHUB pour au final mettre en service et exploiter un site Internet.
Large programme mais tout à fait accessible et ne nécessitant pas de base technique particulière. Juste de l'observation et de la rigueur dans votre travail.

-------------------------------------------------------------------------------------------------------
Séquence 1 : GitHUB
-------------------------------------------------------------------------------------------------------
Objectif : Création d'un Repository GitHUB pour travailler avec son projet  
Difficulté : Très facile (~10 minutes)
-------------------------------------------------------------------------------------------------------
GitHUB est une plateforme en ligne utilisée pour stocker le code de son programme.
GitHUB est organisé en "Repository", c'est à dire en répertoire (contenant lui même des sous répertoires et des fichiers). Chaque Repository sera indépendant les un des autres. Un Repository doit être vu comme un projet unique (1 Repository = 1 Projet). GitHUB est une plateforme très utilisée par les informaticiens.

**Procedure à suivre :**  
1° - Créez vous un compte sur GitHub : https://github.com/  
Si besoin, une vidéo pour vous aider à créer votre propre compte GitHUB : [Créer un compte GitHUB](https://docs.github.com/fr/get-started/onboarding/getting-started-with-your-github-account)  
A noter que **si vous possédez déjà un compte GitHUB, vous pouvez le conserver pour réaliser cet atelier**. Pas besion d'en créer un nouveau.  
Remarque importante : **Lors de votre inscription, utilisez une adresse mail valide. GitHUB n'accepte pas les adresses mails temporaires**  

2° - Faites un Fork du Repository suivant : [https://github.com/OpenRSI/NFA040_Seance1.git](https://github.com/OpenRSI/NFA040_Seance1.git)  
Voici une vidéo d'accompagnement pour vous aider dans les "Forks" : [Forker ce projet](https://youtu.be/p33-7XQ29zQ)    
  
**Travail demandé :** Créé votre compte GitHUB, faites le fork de ce projet et **copier l'URL de votre Repository GitHUB dans la discussion public**.

Notion acquise lors de cette séquence :  
Vous avez appris lors de cette séquence à créer des Repository pour stocker et travailler avec votre code informatique. Vous pourez par la suite travailler en groupe sur un projet. Vous avez également appris à faire des Forks. C'est à dire, faire des copies de projets déjà existant dans GitHUB que vous pourrez ensuite adapter à vos besoins.
  
---------------------------------------------------
Séquence 2 : Création d'un hébergement en ligne
---------------------------------------------------
Objectif : Créer un hébergement sur Alawaysdata  
Difficulté : Faible (~10 minutes)
---------------------------------------------------

Rendez-vous sur **https://www.alwaysdata.com/fr/**  
  
Remarque : **Attention à bien vous rappeler de vos Login/Password** lors de la création de votre compte site car vous en aurez besoin plus tard pour la création de vos Secrets GitHUB.  
  
Voici une vidéo d'accompagnement pour vous aider dans cette séquence de création d'un site sur Alwaysdata : [Vidéo Alwaysdata](https://youtu.be/6jJiqv_ZCHg)  
  
**Procédure :**  
1° - Créez votre compte Alwaysdata (gratuit jusqu'à 100Mo, aucune carte nécéssaire).   
2° - Autoriser les connexions SSH depuis la console d'administration (Le panel d'administration de Alwaysdata):  
 . 2.1 - Cliquez sur SSH (Accès distant).  
 . 2.2 - Modifier les paramètres de votre utilisateur.   
 . 2.3 - Cliquez sur **Activer la connexion par mot de passe**.  
  
**Travail demandé :** Mettre en ligne votre site Internet et **copier l'URL de votre site dans la discussion public**.  
  
Notions acquises lors de cette séquence :  
Vous avez créer un hébergement (gratuit) et découvert également un environnement où pourriez installer bien d'autres applications (Django, Drupal, Jenkins, Magento, Symphony, etc...). Les perspectives sont nombreuses.

---------------------------------------------------------------------------------------------
Séquence 3 : Les Actions GitHUB (Industrialisation Continue)
---------------------------------------------------------------------------------------------
Objectif : Automatiser la mise à jour de votre hébergement Alwaysdata  
Difficulté : Moyenne (~15 minutes)
---------------------------------------------------------------------------------------------
Dans le Repository GitHUB que vous venez de créer précédemment lors de la séquence 1, vous avez un fichier intitulé CICD.yml et qui est déposé dans le répertoire .github/workflows. Ce fichier a pour objectif d'automatiser le déploiement de votre code sur votre site Alwaysdata. Pour information, c'est ce que l'on appel des Actions GitHUB. Ce sont des scripts qui s'exécutent automatiquement lors de chaque Commit dans votre projet (C'est à dire à chaque modification de votre code). Ces scripts (appelés actions) sont au format yml qui est un format structuré proche de celui d'XML.  

Pour utiliser cette Action (CICD.yml), **vous avez besoin de créer des secrets dans GitHUB** afin de ne pas divulguer des informations sensibles aux internautes de passage dans votre Repository comme vos login et password par exemple.  

Pour ce projet Métriques, **vous avez 2 secrets à créer** dans votre Repository GitHUB :  
**USERNAME** : Mettre en secret le login qui est utilisé pour la connexion SSH.  
**PASSWORD** : Mettre en secret le mot de passe qui est utilisé pour la connexion SSH.   
  
Voici une vidéo pour vous expliquer le processus de création de vos secrets dans GitHUB : [Création des secrets](https://youtu.be/Rv5X5-qbvqA) 

Notions acquises de cette séquence :  
Vous avez vu dans cette séquence comment créer des secrets GiHUB afin de mettre en place de l'industrialisation continue.  
L'utilité des scripts d'actions (C'est à dire des scripts exécutés lors des Commits) est très importante mais sortes malheureusement du cadre de cet atelier faute de temps. Toutefois, je vous invites à découvrir cet outil via les différentes sources du Web (Google, ChatGPT, etc..).  

---------------------------------------------------
Séquence 4 : Customisez votre page d'accueil
---------------------------------------------------
Objectif : Créer sa propre page HTML et la mettre en ligne  
Difficulté : Faible (~10 minutes)
---------------------------------------------------
Votre solution est à présent opérationnelle. 
Vous allez à présent modifier votre fichier index.html dans votre Repository afin de customiser votre page d'accueil.

**Travail demandé :** Depuis GitHUB, modifiez votre fichier index.html et remplacer le code de la ligne 8 par celui-ci :  
```<h1>Ceci est mon Site Internet NFA040 </h1>```  
Enregistrez vos modifications via un "Commit" (le gros boutton vert) et observez le résultat en ligne.  

Notions acquises de cette séquence :  
Vous avez apris à modifier votre code depuis GitHUB et mis en ligne votre travail automatiquement.  
