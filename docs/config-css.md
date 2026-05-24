# Petites modifications dans `_config.yml` et le SCSS

## `_config.yml`

Dans la zone `Site Settings`, je recommande :

```yaml
locale                   : "fr-FR"
default_lang             : "fr"
url                      : "https://www.fabienbaeriswyl.fr"
baseurl                  : ""
repository               : "fabienbaeriswyl/fabienbaeriswyl.github.io"
```

## Import SCSS

Si ton fichier `assets/css/main.scss` importe déjà les fichiers `_sass`, ajoute à la fin :

```scss
@import "language-switcher";
```

Si tu préfères éviter l'import, copie directement le contenu de `_sass/_language-switcher.scss` dans ton fichier CSS/SCSS principal.
