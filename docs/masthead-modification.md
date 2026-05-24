# Modification de `_includes/masthead.html`

Dans ton fichier `_includes/masthead.html`, remplace la boucle actuelle :

```liquid
{%- for link in site.data.navigation.main -%}
```

par ce bloc juste avant la boucle :

```liquid
{%- assign current_lang = page.lang | default: site.default_lang | default: "fr" -%}
{%- if current_lang == "en" -%}
  {%- assign nav_links = site.data.navigation.main_en -%}
{%- else -%}
  {%- assign nav_links = site.data.navigation.main_fr -%}
{%- endif -%}
```

Puis fais boucler sur `nav_links` :

```liquid
{%- for link in nav_links -%}
```

Juste après la fin de cette boucle, toujours dans `<ul class="visible-links">`, ajoute :

```liquid
{% include language-switcher.html %}
```

Le résultat doit ressembler à ceci :

```liquid
<ul class="visible-links">
  {%- assign current_lang = page.lang | default: site.default_lang | default: "fr" -%}
  {%- if current_lang == "en" -%}
    {%- assign nav_links = site.data.navigation.main_en -%}
  {%- else -%}
    {%- assign nav_links = site.data.navigation.main_fr -%}
  {%- endif -%}

  {%- for link in nav_links -%}
    <li class="masthead__menu-item">
      <a href="{{ link.url | relative_url }}">{{ link.title }}</a>
    </li>
  {%- endfor -%}

  {% include language-switcher.html %}
</ul>
```
