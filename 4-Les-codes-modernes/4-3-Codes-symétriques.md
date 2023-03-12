# 4.3 Codes symétriques:

Les codes à clé secrète sont les plus employés actuellement car ils sont éprouvés, résistants, rapides et assez facile à mettre en oeuvre. Actuellement leur sécurité est garantie (mais non prouvée) avec des clés assez courtes de 128 à 256 bits pour le standard actuel AES. Mais il faut échanger la clé secrète avec le destinataire d’où un risque. Ils nécessitent un grand nombre de clés. Il faut

$$\frac{n(n-1)}{2}$$

clés pour que $n$ interlocuteurs puissent échanger des informations d’où un problème de fabrication et d’échange de clés fiables.

Ils ont du mal à réaliser sans tiers de confiance le partage des clefs, la signature, l’authentification, et la non répudiation des messages transmis. Ils s’adjoignent parfois un code asymétrique pour cela comme dans le cryptosystème **PGP**.

