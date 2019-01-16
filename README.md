# Rugby Kata

Le but de ce Kata est de générer le classement du TOP14 à partir d'un ancien classement et d'une journée de résultat.

Pour cela, il y a 3 sources de données :
- un CSV du classement après la 13e journée
- un excel des résultat de la 14e journée : Les points marqués par chaque équipe sont inscrits dans les colonnes centrales (3-4) alors que les essais marqués sont donnés dans les colonnes latérales (1-6).
- un CSV avec les noms des équipes : Le nom de l'équipe niveau géographique, le nom commun de l'équipe, le nom officiel de l'équipe

Le format du classement doit être identique à celui en entrée. Ici, il doit donc être identique au classement de la 13e journée mais à jour après la 14e journée.

## Fonctionnement du championnat

La victoire = 4 points
Le match nul = 2 points
La défaite = 0 point
Le bonus = 1 point

Bonus offensif :
Un point bonus est attribué à une équipe inscrivant 3 essais de plus que l'adversaire.

Bonus défensif :
Un point bonus est attribué à une équipe perdant de 5 points ou moins.

Classement (simplifié):
- Nombre de points terrain obtenus sur l'ensemble des rencontres ayant opposé entre elles les équipes concernées (y compris le cas échéant points de bonus et points de pénalisation) ;

## Résultat après la 14e journée

(Ce classement ne reflète pas la réalité à cause de la simplification de classement, Pau va rester ici derrière Toulon)

|Rang|Evol.|Equipe|Pts|J.|G.|N.|P.|Bonus|Pts.M|Pts.E|Diff.|
| -: | --: | --------------: | -: | --: |  -: | -: | -: | -: | --: | --: | ---: | 
| 1  | =   |        Clermont | 52 | 14  | 10  | 2  | 2  | 8  | 463 | 252 | 211  |
| 2  | =   |        Toulouse | 49 | 14  | 10  | 2  | 2  | 5  | 375 | 262 | 113  |
| 3  | =   |     La Rochelle | 42 | 14  | 10  | 0  | 4  | 2  | 349 | 314 | 35   |
| 4  | +   |           Paris | 41 | 14  | 9   | 0  | 5  | 5  | 310 | 272 | 38   |
| 5  | =   |            Lyon | 40 | 14  | 8   | 1  | 5  | 6  | 354 | 269 | 85   |
| 6  | =   |       Racing 92 | 40 | 14  | 9   | 0  | 5  | 4  | 378 | 293 | 85   |
| 7  | -   | Bordeaux-Bègles | 39 | 14  | 8   | 1  | 5  | 5  | 345 | 288 | 57   |
| 8  | +   |         Castres | 33 | 14  | 7   | 0  | 7  | 5  | 274 | 310 | -36  |
| 9  | -   |     Montpellier | 32 | 14  | 6   | 1  | 7  | 6  | 341 | 305 | 36   |
| 10 | =   |          Toulon | 24 | 14  | 5   | 0  | 9  | 4  | 250 | 305 | -55  |
| 11 | +   |             Pau | 24 | 14  | 5   | 0  | 9  | 4  | 276 | 380 | -104 |
| 12 | -   |        Grenoble | 20 | 14  | 3   | 2  | 9  | 4  | 245 | 322 | -77  |
| 13 | =   |            Agen | 17 | 14  | 3   | 1  | 10 | 3  | 220 | 408 | -188 |
| 14 | =   |       Perpignan | 4  | 14  | 0   | 0  | 14 | 4  | 224 | 424 | -200 |


## billes techniques

```python
    pd.set_option('display.max_rows', 500)
    pd.set_option('display.max_columns', 500)
    pd.set_option('display.width', 1000)

    pd.read_csv()
    pd.read_excel()
    
    # delimiter=';', decimal=',', encoding="ISO-8859-1", header=None, names={"colonne1":str,"colonne2":int}
```