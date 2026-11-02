# Aide CommandHMI

Aide en ligne de la configuration CommandHMI, en six langues : anglais, français, italien, allemand, espagnol, néerlandais.

Le site est reconstruit et publié automatiquement par GitHub à chaque modification (onglet **Actions**, environ 2 minutes).

## Modifier une page

1. Sur le site, cliquez sur l'icône crayon en haut à droite de la page. Ou bien, dans ce dépôt, ouvrez le fichier `.md` dans `docs/<langue>/` et cliquez sur le crayon.
2. Corrigez le texte.
3. Cliquez sur **Commit changes**.
4. Le site est à jour environ 2 minutes plus tard. En cas d'échec, l'onglet **Actions** affiche une croix rouge avec le détail de l'erreur.

## Organisation

| Élément | Contenu |
|---|---|
| `docs/en/` | Pages en anglais et toutes les images |
| `docs/fr/`, `docs/it/`, `docs/de/`, `docs/es/`, `docs/nl/` | Pages traduites (elles utilisent les images de `docs/en/`) |
| `mkdocs.yml` | Configuration du site, menu de navigation de chaque langue |
| `.github/workflows/publier.yml` | Construction et publication automatiques |

## Règles à respecter

- Une page modifiée dans une langue ne l'est pas dans les autres : corrigez chaque langue séparément.
- Une nouvelle page `.md` doit aussi être ajoutée au menu de la langue dans `mkdocs.yml` (section `nav` de cette langue).
- Les images ajoutées vont dans `docs/en/`, à côté des images de la même page.
- Tableaux : gardez le même nombre de barres verticales `|` sur chaque ligne.


