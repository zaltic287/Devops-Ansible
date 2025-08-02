

# ANSIBLE : REGEX & RAW


<br>

* regexp_search

```
        {% set url = 'Saliou.blog' %}
        {% if url | regex_search('Saliou') %}
           On est bien là...
        {% else %}
           Je t'invite à voir Saliou
        {% endif %}
```

<br>

* regex_search : insensitif à la case

```
        {% if url | regex_search('Saliou', ignorecase=True) %}
```

---------------------------------------------------------------------------------

# ANSIBLE : REGEX & RAW


<br>

* regex_findall

```
{{ texte | regex_findall('(xav[a-z]*)+')}}
```

<br>

* regex_replace : cas simple

```
        {{ texte | regex_replace('(xav[a-z]*)+','REMPLACEMENT')}}
```

<br>

* regex_replace : avec capture et réutilisation

```
        {{ texte | regex_replace('(xav[a-z]*)+','\1 blog')}}

```

---------------------------------------------------------------------------------

# ANSIBLE : REGEX & RAW

<br>

* regex_replace : suppression

```
        {{ texte | regex_replace('(xav[a-z]*)+')}}

```

<br>

* regex_escape : échappement des caractères spéciaux

```
        {{ '^f.*o(.*)$' | regex_escape() }}
```

---------------------------------------------------------------------------------

# ANSIBLE : REGEX & RAW

<br>

* balises raw

```
  {% raw %}
  {% endraw %}
```
