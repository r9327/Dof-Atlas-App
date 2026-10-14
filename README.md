# Dofus Atlas — application Windows

Ce dépôt **public** est réservé à la distribution de l'application [Dofus Atlas](https://github.com/r9327/Dof-Atlas). Il est distinct du dépôt de développement, qui reste **l'unique source de vérité** pour le code et les données.

## Statut

**Préparation du déploiement. Aucune version stable publiée pour le moment.**

La distribution automatique reste désactivée tant que l'installation sur PC, les mises à jour et la restauration après échec n'ont pas été validées, et que les droits de redistribution des ressources n'ont pas été vérifiés.

## Fonctionnement prévu

- Le dépôt source certifié synchronise ici les seuls éléments nécessaires à l'application (code runtime, données publiables et dépendances). Pas de fichiers de développement, d'outils Doctor/Graphify, de tests ou de profils privés.
- Le fichier `SOURCE_PROVENANCE.json`, généré lors de chaque synchronisation certifiée, identifie le commit source exact. **Son absence signifie qu'aucune synchronisation n'a encore été réalisée.**
- Les fichiers volumineux, l'installateur `DofusAtlasSetup.exe` et le lanceur `DofusAtlas.exe` sont destinés à l'onglet **Releases**, et non à l'historique Git.
- Le lanceur pourra télécharger des mises à jour différentielles et des archives en plusieurs parties, avec contrôles SHA-256 et restauration de la version précédente.
- Les profils, progressions et préférences restent stockés localement sur l'ordinateur de l'utilisateur, en dehors des dossiers remplacés lors des mises à jour.

## Sécurité et mise en service

Le secret de publication `ATLAS_DISTRIBUTION_TOKEN` appartient **uniquement** aux paramètres GitHub Actions de [Dof-Atlas](https://github.com/r9327/Dof-Atlas), jamais à ce dépôt ni à l'application. La variable `ATLAS_DISTRIBUTION_ENABLED` doit rester sur `false` tant que les vérifications finales ne sont pas terminées.

Pour les instructions et la certification Windows, voir [la PR de distribution #159](https://github.com/r9327/Dof-Atlas/pull/159) et [le guide de configuration](https://github.com/r9327/Dof-Atlas/blob/feature/atlas-auto-update-distribution-20261013/docs/distribution/SETUP.md).

Dofus est une marque d'Ankama. Cet outil communautaire n'est pas un produit officiel d'Ankama. Aucune licence n'est accordée ici sur les ressources de tiers ; leurs conditions de redistribution doivent être respectées.
