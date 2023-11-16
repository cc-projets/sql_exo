## 10 Listez pour chaque ticket la quantité totale d’articles vendus. (Classer par quantité décroissante)

```mysql
SELECT numero_ticket, SUM(quantite) AS quantite_total 
FROM ventes
GROUP BY numero_ticket 
ORDER BY quantite_total DESC;
```

## 11 Listez chaque ticket pour lequel la quantité totale d’articles vendus est supérieure à 500. (Classer par quantité décroissante)

```mysql
SELECT numero_ticket, SUM(quantite) AS quantite_total
FROM ventes
GROUP BY numero_ticket
HAVING quantite_total > 500
ORDER BY quantite_total DESC;
```

## 12 Listez chaque ticket pour lequel la quantité totale d’articles vendus est supérieure à 500. On exclura du total, les ventes ayant une quantité supérieure à 50 (classer par quantité décroissante)

```mysql

```

## 13 Listez les bières de type ‘Trappiste’. (id, nom de la bière, volume et titrage)

```mysql
SELECT id_article, nom_article, volume, titrage 
FROM article 
WHERE nom_article 
LIKE '%trappiste%';
```

## 14 Listez les marques de bières du continent ‘Afrique’

```mysql
SELECT nom_marque, continent.nom_continent
FROM marque
INNER JOIN pays ON marque.id_pays = pays.id_pays
INNER JOIN continent ON pays.id_continent = continent.id_continent
WHERE nom_continent = 'Afrique';
```

## 15 Lister les bières du continent ‘Afrique’

```mysql
SELECT nom_article, continent.nom_continent
FROM article
INNER JOIN marque ON article.id_marque = marque.id_marque
INNER JOIN pays ON marque.id_pays = pays.id_pays
INNER JOIN continent ON pays.id_continent = continent.id_continent
WHERE nom_continent = 'Afrique';
```

## 16. Lister les tickets (année, numéro de ticket, montant total payé). En sachant que le prix de vente est égal au prix d’achat augmenté de 15%.

```mysql

```

## 17  Donner le C.A. par année.

```mysql
```

## 18. Lister les quantités vendues de chaque article pour l’année 2016.

```mysql

```

## 19. Lister les quantités vendues de chaque article pour les années 2014, 2015, 2016.

```mysql

```

