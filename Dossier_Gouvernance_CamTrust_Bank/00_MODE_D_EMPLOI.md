# Dossier de gouvernance — CamTrust Bank

> **Bac à sable :** remplacez dans tous les fichiers `Prénom NOM du binôme 1` et `Prénom NOM du binôme 2` par vos noms réels, et `M1 / groupe X` par votre groupe. C'est le premier critère de conformité du rendu : **nom en en-tête**.

---

## 1. Ce que contient ce dossier

| Fichier | Contenu | Étape |
|---|---|---|
| [01_TP1.1_Inventaire_et_classification.md](01_TP1.1_Inventaire_et_classification.md) | Relevés du lab, inventaire des actifs, grille DICP, classification de l'information | TP1.1 |
| [02_TP1.2_Registre_des_risques.md](02_TP1.2_Registre_des_risques.md) | Événements redoutés, sources, scénarios, registre, synthèse d'une page pour la direction | TP1.2 |
| [03_TP1.3_Politique_de_securite_reseau.md](03_TP1.3_Politique_de_securite_reseau.md) | ≥ 25 règles `RES-xx`, couverture des 12 sujets, trace de la revue croisée | TP1.3 |
| [04_TP1.3_Grille_de_controle.md](04_TP1.3_Grille_de_controle.md) | Grille d'audit déroulée sur le lab + captures d'écran légendées | TP1.3 |
| `captures/` | Les captures d'écran, une par vérification, recadrées | TP1.3 |

**Dépendances entre les fichiers :** l'inventaire (01) alimente les scénarios (02) ; les risques (02) sont référencés par les règles (03) ; les preuves de contrôle (03) deviennent la grille d'audit (04). Ne remplacez pas les identifiants en cours de route.

## 2. Format de rendu

- **Un seul fichier** (PDF ou Word) avec le nom des deux membres du binôme en en-tête.
- Le dépôt Git du binôme contient le dossier complet ; le fichier unique est le compte rendu.
- **Une capture par vérification demandée**, recadrée sur l'essentiel et légendée. Ce qui dépasse la limite de pages n'est pas lu.
- Politique de sécurité réseau : **15 pages au maximum**. Trop long = pas lu.

> ⚠️ **À confirmer avec l'enseignant avant de tout comprimer :** l'énoncé affiche « 5 pages au plus, un seul fichier » en tête de chapitre, alors que la politique seule peut faire 15 pages et que Google Classroom accepte « documents, captures, archives, même volumineux ». Lecture la plus probable : dépôt Git + archive Classroom = dossier complet (4 pièces) ; le fichier unique ≤ 5 pages = compte rendu de synthèse avec captures légendées.

## 3. Les deux erreurs éliminatoires

1. **Règles copiées d'un modèle sans adaptation à CamTrust Bank.** Chaque règle doit nommer un actif, un site ou un service réel : core banking, passerelle Mobile Money, monétique (cartes et distributeurs), messagerie, site web, Wi-Fi clients en agence, agences de Douala et Garoua, VPN des agences, R-SIEGE, R-DLA, 4 administrateurs, 2 prestataires.
2. **Référence légale inventée.** Utilisez uniquement ces deux titres, vérifiés :
   - **Loi n° 2010/012 du 21 décembre 2010 relative à la cybersécurité et à la cybercriminalie au Cameroun** → journalisation et conservation.
   - **Loi n° 2024/017 du 23 décembre 2024 relative à la protection des données à caractère personnel au Cameroun** → flux de données personnelles vers l'étranger.

## 4. Règles d'écriture appliquées dans ces fichiers

- **Les identifiants `RES-xx` sont stables.** Ils sont cités dans les comptes rendus de **tous les TP suivants** et vérifiés à l'audit final (M13). Ne jamais en changer, ne jamais en sauter, ne jamais réutiliser un identifiant supprimé.
- **Une règle = une vérification possible.** Si vous ne pouvez pas écrire la commande ou la méthode qui la prouve, la règle n'est pas encore rédigée.
- **La criticité d'un actif = le niveau le plus élevé de sa grille DICP.** Pas d'avis technique.
- **Les justifications sont métier, pas techniques** : « relevés indisponibles 2 h = réclamation client et saisie de l'ACMC », pas « c'est critique ».

## 5. Checklist avant de rendre

- [ ] Noms du binôme dans l'en-tête de chaque document
- [ ] Inventaire ≥ 20 lignes, chaque bien support relié à au moins une valeur métier
- [ ] Chaque actif a un propriétaire nommé **par sa fonction**
- [ ] Grille DICP des 6 services justifiée par conséquence métier ; criticité reportée dans l'inventaire
- [ ] 10 types d'informations classés + 2 règles réseau par niveau
- [ ] ≥ 6 scénarios de risque, dont les 3 imposés (fraude interne sur le lien agence, rançongiciel via un poste d'agence, indisponibilité du lien Internet un jour de paie)
- [ ] Chaque scénario s'appuie sur des biens supports de l'inventaire ; niveau calculé ; traitements avec au moins une mesure réseau, un responsable, une échéance
- [ ] Synthèse d'une page chiffrée en FCFA, sans jargon, prête pour 3 minutes de présentation orale
- [ ] ≥ 25 règles, couverture des 12 sujets, chaque règle avec preuve de contrôle
- [ ] Remarques de la revue croisée écrites et traitées (acceptée ou refusée **avec justification**)
- [ ] Grille de contrôle déroulée sur ≥ 5 règles avec captures légendées
- [ ] Aucune règle générique non adaptée à CamTrust Bank
- [ ] Aucune référence légale inventée

## 6. Commandes utiles

```bash
# Convertir en Word (pandoc est installé sur cette machine)
pandoc 01_TP1.1_Inventaire_et_classification.md -o TP1.1_Inventaire.docx

# Convertir tous les fichiers en un seul document
pandoc 00_MODE_D_EMPLOI.md 01_TP1.1_Inventaire_et_classification.md \
        02_TP1.2_Registre_des_risques.md 03_TP1.3_Politique_de_securite_reseau.md \
        04_TP1.3_Grille_de_controle.md -o Dossier_Gouvernance_CamTrust_Bank.docx
```
