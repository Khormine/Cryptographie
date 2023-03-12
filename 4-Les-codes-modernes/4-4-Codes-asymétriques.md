# 4.4 Codes asymétriques:

Ils ont dégagé la notion de fonction à sens unique. Ce sont des fonctions qui sont faciles à calculer c’est à dire calculable en temps polynomial en fonction de la taille des données mais tel que la fonction inverse ne soit pas calculable en temps polynomial en fonction de la taille des données.

Un problème de la classe **NP** est un problème dont la solution exige un calcul en temps non polynomial en fonction de la taille des données, sous réserve de la validité de la conjecture $P \neq NP$.

Les cryptosystèmes asymétriques reposent sur des structures mathématiques élaborées. Leur sûreté est bonne mais non prouvée. Leur cryptanalyse dépend beaucoup des progrès des mathématiques correspondantes.

Sauf pour les codes elliptiques, ils nécessitent des clés longues (1024 à 2048 bits) pour avoir une sûreté équivalentes à celle d’un cryptosystème à clef secrète de 128 à 256 bits. Ils sont 1000 à 1500 fois plus lents. Mais ils permettent de réaliser facilement les fonctionnalités suivantes:
- partage des clés
- authentification
- intégrité
- non répudiation
et bien d’autres encore grâce au fait que la clef est en fait constituée de deux clefs, la clef de codage et la clef de décodage, et que cette dernière est attachée à une personne et la caractérise.

Ils ne nécessitent que $n$ paires de clés (une clé secrète et une clé publique) pour $n$ interlocuteurs.

On les utilise souvent pour la transmission des clés secrètes des codes symétriques