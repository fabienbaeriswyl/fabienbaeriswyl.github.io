# Front matter recommandé pour tes pages bilingues

Le principe est simple : chaque paire de pages porte le même `ref`, mais une langue différente. `translation_url` est explicite, donc robuste.

## Accueil

`index.html` :

```yaml
---
layout: home
author_profile: true
permalink: /
lang: fr
ref: home
translation_url: /en/
markdown: false
---
```

`en/index.html` :

```yaml
---
layout: home
author_profile: true
permalink: /en/
lang: en
ref: home
translation_url: /
markdown: false
---
```

## Publications

`_pages/publi.md` :

```yaml
---
layout: home
title: "Publications et intérêts de recherche"
permalink: /publi/
author_profile: true
lang: fr
ref: publications
translation_url: /en/publications/
---
```

`_pages/publi-en.md` :

```yaml
---
layout: home
title: "Publications and research interests"
permalink: /en/publications/
author_profile: true
lang: en
ref: publications
translation_url: /publi/
---
```

## Communications / Talks

`_pages/conf.md` :

```yaml
---
layout: home
title: "Conférences et colloques"
permalink: /conf/
author_profile: true
lang: fr
ref: talks
translation_url: /en/talks/
---
```

`_pages/conf-en.md` :

```yaml
---
layout: home
title: "Conferences and workshops"
permalink: /en/talks/
author_profile: true
lang: en
ref: talks
translation_url: /conf/
---
```

## À propos / About

`_pages/apropos.md` :

```yaml
---
layout: home
title: "À propos de moi"
permalink: /apropos/
author_profile: true
lang: fr
ref: about
translation_url: /en/about/
---
```

`_pages/about-en.md` :

```yaml
---
layout: home
title: "About me"
permalink: /en/about/
author_profile: true
lang: en
ref: about
translation_url: /apropos/
---
```

## Collègues / Colleagues

`_pages/collegues.md` :

```yaml
---
layout: home
title: "Ami.e.s, collègues et liens"
permalink: /collegues/
author_profile: true
lang: fr
ref: colleagues
translation_url: /en/colleagues/
---
```

`_pages/colleagues.md` :

```yaml
---
layout: home
title: "Colleagues, friends and links"
permalink: /en/colleagues/
author_profile: true
lang: en
ref: colleagues
translation_url: /collegues/
---
```

Ensuite, supprime la première ligne manuelle du type `[:uk: Click here...]` ou `[:fr: Cliquez ici...]` dans chaque page : le bouton du header la remplace.
