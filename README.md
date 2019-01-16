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
- Goal-average sur l'ensemble des rencontres de la compétition ;

## billes techniques

```python
    pd.set_option('display.max_rows', 500)
    pd.set_option('display.max_columns', 500)
    pd.set_option('display.width', 1000)

    pd.read_csv()
    pd.read_excel()
    
    # delimiter=';', decimal=',', encoding="ISO-8859-1", header=None, names={"colonne1":str,"colonne2":int}
```