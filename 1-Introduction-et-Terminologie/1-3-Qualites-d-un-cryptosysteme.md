# 1.3 Qualités d’un cryptosystème:

Les qualités demandées à un système cryptographique sont résumées par les mots clefs suivants:
- **Confidentialité**: seules les personnes habilitées ont accès au contenu du message.
- **Intégrité des données**: le message ne peut pas être falsifié sans qu’on s’en aperçoive.
- **Authentification**:
  - l’émetteur est sûr de l’identité du destinataire c’est à dire que seul le destinataire pourra prendre connaissance du message car il est le seul à disposer de la clef de déchiffrement.
  - le receveur est sûr de l’identité de l’émetteur
- **Non-répudiation**:
  - non-répudiation d’origine l’émetteur ne peut nier avoir écrit le message et il peut prouver qu’il ne l’a pas fait si c’est effectivement le cas
  - non-répudiation de réception le receveur ne peut nier avoir reçu le message et il peut prouver qu’il ne l’a pas reçu si c’est effectivement le cas.
  -  non-répudiation de transmission l’émetteur du message ne peut nier avoir envoyé le message et il peut prouver qu’il ne l’a pas fait si c’est effectivement le cas.