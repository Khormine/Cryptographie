# 4.5 Les échanges de clefs:

Un problème important rencontré dans l’utilisation d’un cryptosystème est l’échange des clefs entre des interlocuteurs. C’est un des moments où la sécurité du cryptosystème est la plus vulnérable. Il faut trouver un protocole sûr pour l’échange des clefs.

Rappelons que dans un cryptosystème à clef secrète lorsque deux interlocuteurs veulent converser il leur faut échanger une clef. Il faut donc autant de clefs qu’il y a de paires non ordonnées d’interlocuteurs. Le nombre de clefs à échanger entre $n$ interlocuteurs est donné par:

<!-- TODO IMG -->

Par contre dans un système à clef publique il faut autant de paires de clefs qu’il y a d’interlocuteurs. Chaque interlocuteur dispose en effet d’une clef publique qui figure dans un annuaire et que n’importe qui peut utiliser pour crypter les messages qui lui sont adressés et d’une clef privée, strictement personnelle, pour décrypter les messages qu’il re¸coit.

Le protocole d'échange de clefs utilise de l’arithmétique modulaire dans les entiers modulo un nombre premier p. L'alogorithme est le suivant:
1. Alice et Bob choisissent d’un commun accord sur une ligne non protégée un grand nombre premier $p$ et $\alpha$ un générateur de $(\mathbb{Z}/p\mathbb{Z})^*$
2. Alice choisit $a$ et calcule $\alpha^a = \alpha_a\ (mod\ p)$
3. Bob choisit $b$ et calcule $\alpha^b = \alpha_b\ (mod\ p)$
4. Alice et Bob échangent $\alpha_a$ et $\alpha_b$ sur un canal non nécessairement protégé
5. Alice calcule $\alpha^a_b\ (mod\ p)$ et Bob calcule $\alpha^b_a\ (mod\ p)$

On a  

$$\alpha^a_b \equiv \alpha^{ba} \equiv  \alpha^b_a\ (mod\ p)$$

c’est la clef commune d’Alice et Bob.

Pourquoi ce protocole est-il sûr? Si Eve intercepte la communication entre Alice et Bob, elle peut lire les nombres $\alpha_a$ et $\alpha_b$.
Pour calculer la clef commune d’Alice et de Bob, il faut qu’Eve puisse calculer $\alpha^{ab}$ à partir de $\alpha^a$ et $\alpha^b$ en connaissant $\alpha$. La seule méthode connue actuellement est de trouver $a$ et $b$ à partir de $\alpha^a$ et $\alpha^b$, c’est à dire qu’elle puisse calculer le logarithme discret dans $\mathbb{F}_p$.

Pour l’instant il n’existe pas d’algorithme rapide, c’est à dire polynomial en temps en fonction de la taille des données, pour calculer le logarithme discret dans $\mathbb{F}_p$.