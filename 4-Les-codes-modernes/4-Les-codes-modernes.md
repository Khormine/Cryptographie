# 4. Les codes modernes:

**Définition 4.0.1:** Un cryptosystème est un dictionnaire entre les messages en clair et les messages chiffrés.

**Définition 4.0.2:** Un cryptosystème est un quintuplet $(P,C,K,\epsilon,D)$ où:
- $P$ est un ensemble fini de blocs: les **mots en clairs**
- $C$ est un ensemble fini de blocs: les **mots codés**
- $K$ est un ensemble : l'**espace des clés**
- Pour tout  $k \in K$, on a une **règle de chiffrement** $e_k \in \epsilon$ et une **règle de déchiffrement** correspondante $d_k \in D$. Chaque $e_k : P \rightarrow C$ et $d_k : C \rightarrow D$ sont des fonctions telles que $d_k(e_k(x)) = x$ pour tout $x \in P$

Un code moderne est donc constitué:
- D’un algorithme de chiffrement $f = f_{k_C}$, supposé connu de tous, dépendant d’un paramètre $k_C$, la clé de chiffrement. L’algorithme est fixé et public, seule la clé change, (on applique le principe de Kerckhoffs).
- De la valeur de la clé de chiffrement, $k_C$ qui est secrète ou non suivant que l’on a affaire à un code à clef secrète ou à un code à clef publique.
- D’un algorithme de déchiffrement $g = g_{K_D} = f^{−1}$ (supposé connu de tous) dépendant d’une clé de déchiffrement, $k_D$, différente ou non de $k_C$.
- De la valeur de la clé de déchiffrement, $k_D$, qui est toujours secrète