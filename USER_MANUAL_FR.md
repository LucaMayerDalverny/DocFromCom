# Manuel d'utilisation de DocFromCom

## Sommaire

1. [Génération de documentation](#generateur)
    1. [Commande](#generateurcommande)
    2. [Écriture des commentaires](#generateurcommentaires)

## Génération de documentation <a name="#generateur"></a>

### Commande <a name="#generateurcommande"></a>

```bash
php DocFromCom.phar document:generate "Chemin/Monfichier" "ExtensionDuFichier" md FR
```

### Écriture des commentaires <a name="#generateurcommentaires"></a>

#### En-tête du fichier

Pour générer l'en-tête du document, il faut faire un commentaire multiligne comme celui suivant :  

```c
/**
 * @title Nom du fichier
 * @docauthor Votre nom
 * @date la date de création du fichier
 * @make
 */
```

Les balises `@title`, `@docauthor` et `@date` peuvent être mise dans n'importe quel ordre. Si la balise `@date` est manquante, la date du jour sera ajouté à l'en-tête du document.

#### Structures de données

Pour faire la documentation d'une structure de données, plusieurs balises sont disponibles :

+ `@struct` : Nom de la structure
+ `@desc` : Description de la structure
+ `@author` : Nom de l'auteur de la structure (inutile si le fichier a été rédigé par une seule personne)
+ `@field` : Description d'un champ de la structure

L'utilisation de ces balises se fait comme dans l'exemple suivant :  

```c
/**
 * @struct MaStruct
 * @desc Description de la structure
 * @field premierChamp (int) : description du champ
 * @field secondChamp (float) : description du champ
 */
typedef struct MaStruct
{
    int premierChamp;
    float secondChamp;
}MaStruct;
```

#### Fonctions

Pour la documentation des fonctions, les balises suivantes sont disponibles :

+ `@fn` : Nom de la fonction
+ `@desc` : Rôle de la fonction
+ `@author` : Nom de l'auteur de la fonction (inutile si le fichier a été rédigé par une seule personne)
+ `@param` : Description d'un paramètre de la fonction
+ `@return` : Description de la valeur de retour de la fonction

Les balises `@bcode` et `@ecode` permettent d'ajouter le prototype de la fonction avec la coloration syntaxique à la documentation (c'est facultatif mais plus joli). Toute les balise sont à utiliser comme dans l'exemple qui suit :  

```c
/**
 * @fn maFonction
 * @desc Description de la fonction
 * @author Nom de l'auteur
 * @param premierParametre (int) : description
 * @param secondParametre (int) : description
 * @return (float) : description du retour de la fonction
 * @bcode
 */
float maFonction(int premierParametre, int secondParametre);
/**
 * @ecode
 */
```

