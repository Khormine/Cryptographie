# 1.4 Attaques sur un chiffrement:

La cryptanalyse est l’ensembles des procédés d’attaque d’un cryptosystème. Elle est indispensable pour l’étude de la sécurité des procédés de chiffrement utilisés en cryptographie. Son but ultime est de trouver un algorithme de déchiffrement des messages. Le plus souvent on essaye de reconstituer la clef secrète de déchiffrement.

On suppose, en vertu des principes de Kerckhoffs, pour toutes les évaluations de sécurité d’un cryptosystème que l’attaquant connait le système cryptographique utilisé, la seule partie secrète du cryptosystème est la clef.

On doit distinguer entre les types d’attaques d’un adversaires et les buts des attaques d’un adversaire. Les principaux types d’attaques:
- **attaque à texte chiffré connu**: l’opposant ne connait que le message chiffré y.
- **attaque à texte clair connu**: l’opposant dispose d’un texte clair x et du message chiffré correspondant y
- **attaque à texte clair choisi**: l’opposant a accès à une machine chiffrante. Il peut choisir un texte clair et obtenir le texte chiffré correspondant y, mais il ne connait pas la clef de chiffrement
- **attaque à texte chiffré choisi**: l’opposant a accès à une machine déchiffrante. Il peut choisir un texte chiffré, y et obtenir le texte clair correspondant x, mais il ne connait pas la clef de déchiffrement

En plus de ces attaques basées sur une étude de messages codés, il y a aussi des attaques physiques. Le principe de ces attaques est d’essayer de reconstituer la clef secrète par exemple en espionnant la transmission entre le clavier de l’ordinateur et l’unité centrale ou en mesurant la consommation électrique du microprocesseur qui effectue le décodage du message ou encoreen mesurant son échauffement. Ensuite on essaye de remonter de ces données physiques aux clefs de codage et décodage. Une méthode pour résister à ce type d’attaque sont les protocoles de preuve sans transfert de connaissance (zero-knowledge proof).

Garantir la confidentialité des communications entre Alice et Bob suppose donc qu’Eve ne peut pas:
- trouver $M$ à partir de $E(M)$ (le crypto-système doit être résistant aux attaques sur le message codé)
- trouver la méthode de déchiffrement $D$ à partir d’une famille de couples, ${(M_i, E(M_i)}$, (message clair, message codé correspondant)
- accéder à des données contenues dans le micro-processeur qui code et décode et plus généralement ne puisse pas espionner les ordinateurs d’Alice et de Bob