# walid924.github.io

Code source de mon portfolio : labs, veille technologique et certifications en systèmes et réseaux.

Site en ligne : **https://walid924.github.io**

## Organisation

```
.
├── .github/workflows/docs.yml   Publication automatique sur GitHub Pages
├── docs/                        Contenu du site (Markdown)
│   ├── index.md                 Accueil
│   ├── a-propos.md              Parcours, compétences, contact
│   ├── certifications.md
│   ├── labs/                    Un fichier par lab
│   ├── veille/                  Un fichier par article (AAAA-MM-titre.md)
│   └── assets/
│       ├── documents/           CV et attestations (PDF)
│       ├── img/                 Captures et schémas
│       └── stylesheets/         Feuille de style personnelle
├── modeles/                     Modèles à copier (non publiés)
├── requirements.txt             Version de Zensical
└── zensical.toml                Configuration du site et menu
```

## Lancer le site en local

```bash
python -m venv .venv
source .venv/bin/activate        # Windows : .venv\Scripts\activate
pip install -r requirements.txt
zensical serve
```

Le site est alors visible sur http://localhost:8000 et se met à jour à chaque sauvegarde.

## Ajouter un contenu

1. Copier `modeles/lab.md` dans `docs/labs/` (ou `modeles/veille.md` dans `docs/veille/`).
2. Renommer le fichier en minuscules avec des tirets : `vlan-packet-tracer.md`, `2026-11-ransomware-pme.md`.
3. Ajouter la page dans `nav` (fichier `zensical.toml`) et dans le tableau de la rubrique (`index.md`).
4. Vérifier avec `zensical serve`, puis publier :

```bash
git add .
git commit -m "Ajout du lab VLAN"
git push
```

## Conventions

- Noms de fichiers : minuscules, tirets, sans accents.
- Images : `docs/assets/img/<lab>-<numéro>-<description>.png`, par exemple `ad-01-installation.png`.
- Aucune donnée réelle d'entreprise, aucun mot de passe, aucune adresse IP publique.
- Messages de commit courts, au présent : « Ajout du lab AD », « Correction de la page certifications ».
