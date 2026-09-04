# Configurations machines

Dépôt public contenant les configurations et les profils validés des équipements du Fab Lab du Cégep Limoilou.

> Important : ce dépôt est public. Aucun mot de passe, jeton, certificat privé, renseignement personnel ou chemin propre à un utilisateur ne doit y être publié.

## Organisation des téléchargements

Les fichiers utilisés par les boutons de téléchargement du site se trouvent dans le dossier `telechargements`.

```text
telechargements/
└── CODE/
    └── CODE_description.zip
```

Le code représente la cellule ou la catégorie de rattachement de l’équipement. Par exemple :

* `C00` : postes informatiques
* `C01` : fraiseuse CNC 96 × 48 po
* `C02` : découpeuses laser
* `C03` : imprimantes 3D FDM
* `C04` : imprimante 3D SLA
* `C06` : microfraiseuse 5 axes

Les dossiers sont créés uniquement lorsqu’une première configuration validée doit y être publiée.

## Convention de nommage

Le fichier officiel conservé dans une version GitHub suit cette convention :

```text
CODE_AAMMJJ_description.zip
```

Règles :

* `CODE` correspond à la cellule ou à la catégorie;
* `AAMMJJ` correspond à la date du renommage et de la validation;
* la description est écrite en minuscules;
* les accents et les espaces sont retirés;
* les mots sont séparés par des traits d’union;
* l’extension est écrite en minuscules;
* les termes comme `final`, `nouveau`, `copie`, `latest` et `v2` ne sont pas utilisés.

Exemple de fichier officiel archivé :

```text
C03_260904_profil-bambu-h2d-pro-petg.zip
```

## Alias stable pour le site web

Le fichier placé dans `telechargements` omet volontairement la date :

```text
C03_profil-bambu-h2d-pro-petg.zip
```

Il s’agit d’un alias de distribution stable. Son contenu est remplacé par la dernière version approuvée, mais son nom et son adresse demeurent inchangés.

La copie datée constitue l’archive officielle et doit être conservée dans une version GitHub.

## Adresse de téléchargement

Le modèle d’adresse utilisé par le site est :

```text
https://raw.githubusercontent.com/FabLab-Cegep-Limoilou/configurations-machines/main/telechargements/CODE/CODE_description.zip
```

Exemple :

```text
https://raw.githubusercontent.com/FabLab-Cegep-Limoilou/configurations-machines/main/telechargements/C03/C03_profil-bambu-h2d-pro-petg.zip
```

Cette adresse pointe vers la version actuellement approuvée dans la branche `main`.

## Procédure de publication

1. Tester la configuration sur l’équipement approprié.
2. Examiner le contenu du fichier ZIP sans exécuter les scripts qu’il contient.
3. Vérifier l’absence de secrets, de renseignements personnels et de chemins propres à un utilisateur.
4. Nommer la copie officielle selon la convention `CODE_AAMMJJ_description.zip`.
5. Mettre à jour l’alias stable correspondant dans `telechargements/CODE/`.
6. Effectuer la modification dans une nouvelle branche.
7. Ouvrir une pull request et documenter l’équipement, le logiciel et les essais réalisés.
8. Faire approuver la pull request par une autre personne.
9. Fusionner la pull request avec la méthode `Squash`.
10. Créer une version GitHub contenant la copie officielle datée.
11. Tester le lien brut et le bouton de téléchargement du site.

## Modification du dépôt

La branche `main` est protégée. Toute modification doit passer par une pull request approuvée avant sa publication.
