# 1.5 Différentes notions de sécurité:

- La sécurité inconditionnelle qui ne préjuge pas de la puissance de calcul du cryptanalyste qui peut être illimitée
- La sécurité calculatoire qui repose sur l’impossibilité de faire en un temps raisonnable, compte tenu de la puissance de calcul disponible, les calculs nécessaires pour décrypter un message.  Cette notion dépend de l’état de la technique à un instant donné.
- La sécurité prouvée qui réduit la sécurité du cryptosystème à un problème bien connu réputé difficile, par exemple on pourrait prouver un théorème disant qu’un système cryptographique est sˆur si un entier donné n ne peut pas être factorisé.
- La confidentialité parfaite qualité des codes pour lesquels un couple (message clair, message chiffré) ne donne aucune information sur la clef.

Toutes ces notions de sˆureté reposent sur la **théorie de l’information** de Claude Shannon et la notion de sécurité calculatoire repose sur la **théorie de la complexité**.  C’est la sécurité calculatoire que l’on utilise dans la plupart des évaluations de sécurité des systèmes cryptographiques.

La sécurité prouvée consiste à ramener la sécurité d’un cryptosystème à un problème que l’on sait ou que l’on espère être calculatoirement difficile comme par exemple la factorisation des entiers en facteurs premiers. Ceci permet de classifier les différents cryptosystèmes suivant leur sécurité et de procéder à une veille technologique rationnelle.