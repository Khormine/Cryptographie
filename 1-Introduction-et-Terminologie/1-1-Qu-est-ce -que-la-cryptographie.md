# 1.1 Qu’est ce que la cryptographie:

La cryptographie ou science du secret est un art très ancien, c’est **l’art de remplacer un secret encombrant par un secret miniature**. Le secret encombrant est le contenu du message il est remplacé par un petit secret qui est la clef de déchiffrement dont la taille est en général de quelques centaines à quelques milliers de bits à comparer aux mégabits d’un message.

La *cryptographie* est l’art de rendre inintelligible, de crypter, de coder, un message pour ceux qui ne sont pas habilités à en prendre connaissance. Le chiffre, le code est le procédé, l’algorithme, la fonction, qui permet de crypter un message.

La *cryptanalyse* est l’art pour une personne non habilitée, de décrypter, de décoder, de déchiffrer, un message. C’est donc l’ensemble des procédés d’attaque d’un système cryptographique.

La *cryptologie* est l’ensemble formé de la cryptographie et de la cryptanalyse.

La cryptologie fait partie d’un ensemble de théories et de techniques liées à la transmission de l’information (théorie des ondes électro-magnétiques, théorie du signal, théorie des codes correcteur d’erreurs, théorie de l’information, théorie de la complexité,...).

Un expéditeur Alice veut envoyer un message à un destinataire Bob en évitant les oreilles indiscrète d’Eve, et les attaques malveillantes de Martin. Pour cela Alice se met d’accord avec Bob sur le cryptosystème qu’ils vont utiliser.

L’information qu’Alice souhaite transmettre à Bob est le texte clair. Le processus de transformation d’un message, M, pour qu’il devienne incompréhensible à Eve est appelé le chiffrement ou la codage. On génère ainsi un message chiffré, C, obtenu grˆace à une fonction de chiffrement, $E$, par 
$$C = E(M)$$

Le processus de reconstruction du message clair à partir du message chiffré est appelé le déchiffrement ou décodage et utilise une fonction de déchiffrement, $D$. On demande que pour tout message clair $M$
$$ D(C) = D(E(M)) = M$$

Un algorithme cryptographique est l’ensemble des fonctions (mathématiques ou non) utilisées pour le chiffrement et le déchiffrement. En pratique les
fonctions E et D sont paramétrées par des clés, $K_e$ la clé de chiffrement et $K_d$ la clef de déchiffrement, qui peuvent prendre l’une des valeurs d’un
ensemble appelé espace des clefs. On a donc la relation suivante

$$\left\{
    \begin{array}{rcr}
        E_{K_e}(M) = C \\
        D_{K_d}(C) = M
    \end{array}
\right.$$

Le type de relation qui unit les clés $K_e$ et $K_d$ permet de définir deux grandes catégories de systèmes cryptographiques:
- Les systèmes à clef secrètes ou symétriques: (DES, AES, IDEA, Blowfish,...)
- Les systèmes à clefs publiques ou asymétriques: (RSA, El-Gamal, un cryptosystème elliptique,...)

En outre les fonctions de codage $E$ et de décodage $D$ peuvent fonctionner de deux fa¸cons:
- **en continu**: chaque nouveau bit est manipulé directement
- **par bloc**: chaque message est d’abord partitionné en blocs de longueur fixe. Les fonctions de chiffrement et déchiffrement agissent alors sur chaque bloc.

Chacun de ces systèmes dépend d’un ou deux paramètres de taille assez réduite (128 à 2048 bits) appelés la clef de chiffrement et la clé de déchiffrement. Les clefs de chiffrement et de déchiffrement n’ont aucune raison d’être identiques. Seule la clef de déchiffrement doit impérativement être secrète.