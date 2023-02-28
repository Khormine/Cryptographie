# 3. Quelques méthodes de codage:

Les systèmes de chiffrement par blocs agissent sur les données avec une transformation fixe des grands blocs de données en clair; les systèmes de chiffrement par flots (ou chiffrement par flux) agissent avec une transformation variant avec le temps sur des données en clair individuelles.

Le chiffrement par blocs est le plus répandu et jouit d’une meilleure réputation que le chiffrement par flots plus facile à analyser mathématiquement. Le schéma général du chiffrement par blocs symétrique ou à clef secrète est le suivant:
1. coder l’information source en binaire. On obtient ainsi une chaîne de caractères composée de 0 et de 1.
2. découper cette chaîne en blocs de longueur donnée (par exemple 64 bits ou 128 bits ou 256 bits).
3. chiffrer un bloc en faisant un OU exclusif (ou XOR) bit à bit avec une clé secrète, k, qui est une suite de 0 et de 1 de même longueur.
4. déplacer et permuter certains bits du bloc.
5. recommencer un certain nombre de fois l’étape précédente, on appelle cela une **ronde**
6. passer au bloc suivant et retourner à l’étape 3 jusqu’à ce que tous les blocs soient chiffrés.

Le schéma général de chiffrement par blocs asymétrique ou à clef publique est le suivant:
1. coder l’information source en binaire. On obtient ainsi une chaîne de caractères composée de 0 et de 1.
2.  découper cette chaîne en blocs de longueur donnée (par exemple 1024 bits à 2048 bits pour RSA et El Gamal, 256 bits pour les codes elliptiques).
3.  chiffrer un bloc en utilisant la fonction de chiffrement (exponentiation modulaire pour RSA).
4.  passer au bloc suivant et retourner à l’étape 3 jusqu’à ce que tous les blocs soient chiffrés.

Le problème pratique qui se pose ensuite est le protocole d’envoi des blocs successivement obtenus. Il faut que ce protocole ne diminue pas la sureté du cryptosystème.