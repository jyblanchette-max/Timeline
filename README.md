# Ligne du temps biblique

Placer `index.html`, `config.json` et `rois.csv` dans le même dossier sur un hébergement web statique. Ouvrir la page via HTTP/HTTPS. Le double-clic local nécessite une sélection manuelle des CSV.

`rois.csv` contient 54 entrées concernant les rois et les royaumes, dont 48 périodes. Les dates, leurs approximations et les notes de provenance jw.org sont conservées. Une fin déduite d’un repère de succession est signalée dans `note_dates`.

Pour ajouter un groupe, créer par exemple `prophetes.csv` avec les mêmes colonnes, puis ajouter dans la liste `groupes` de `config.json` :

```json
{"id": "prophetes", "nom": "Prophètes", "fichier": "prophetes.csv"}
```

Les CSV doivent rester dans le même dossier. Chaque entrée doit garder un identifiant unique dans tous les fichiers. Les cases de groupe permettent les comparaisons ; les catégories permettent de distinguer les royaumes. Si un fichier échoue, le chargement entier est refusé et les données précédentes restent affichées.

Les imports manuels remplacent les données de la session. L’export réunit tous les groupes chargés dans un CSV. Aucune modification depuis la page n’est écrite sur le serveur.

Projet personnel, non officiel. Le dépôt GitHub stocke les fichiers ; leur publication en site web est une étape distincte.
