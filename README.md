# easy_epi_calendar
La saisie des temps Fitnet est parfois fastidieuse. Cet outil va permettre de  simplifier la saisie des temps dans Fitnet en récuppérant les saisies et réunions de Google Calendar de la **semaine passée** et d'en faire un JSON facile à lire et comprendre. L'outil en question est développé en Python mais ne demande pas une grande expertise en développement pour le lancer.

## Pré-requis
- Python

Il faut avoir Python sur votre machine. Peut importe la version mais je vous conseille d'avoir la dernière en date. 

> [!TIP]
> Selon le système d'exploitation de votre machine, il y a des différences d'installation. Il existe plusieurs ressources possibles : Documentation, Vidéos Youtube etc... 

Après avoir installé Python, il vous faut avoir un environnement virtuel. L'environnement virtuel est comme un bac à sable dans lequel vous allez avoir des jouets spécifiques qui sont des packages/librairies. On ne veut pas jouer directement sur la plage qui est le Python installé, mais on veut délimiter et avoir un petit bac à sable ici c'est l'environnement virtuel. La commande pour générer l'environnement virtuel :

- venv 
```
python -m venv .venv
```

Selon le système d'exploitation il va falloir activer cet environnement et installer les packages qui se trouvent dans le fichier ```requirements.txt```

Linux : 
```bash
source .venv/bin/activate
# Si un (.venv) apparaît c'est que votre environnement est activé
pip install -r requirements.txt
```

Windows :
```Powershell
& .venv\Scripts\activate
# Si un (.venv) apparaît c'est que votre environnement est activé
pip install -r requirements.txt
```

Dans les deux cas pour désactiver l'environnement virtuel il vous suffit de tapper la commande : ```deactivate```. 

- ```credentials.json```

Après avoir tout installé correctement il vous faut aussi le fichier ```credentials.json```. C'est un fichier important pour savoir quel projet et authentification utiliser pour autoriser l'application à accéder à vos informations sur Google Calendar. Générez d'abord un dossier ```data``` puis ajouter le fichier dedans (si le fichier n'est pas disponible sur le repo demander à Charles VU). 

## Lancement du programme 
Pour lancer le programme il faut d'abord activer votre environnement virtuel puis lancer la commande suivante : 

```
python main.py
```

Si vous lancez le programme pour la première fois vous serez invité à suivre un liens et valider votre compte Google pour générer le fichier ```token.json``` dans le dossier ```data```. Ce token va permettre de vous identifier et récupérer votre Google Calendar. 

> [!WARNING]
> Seulement les collaborateurs d'Epiconcept sont autorisés à utiliser l'outil si vous utiliser un autre compte Google cela ne marchera pas!

