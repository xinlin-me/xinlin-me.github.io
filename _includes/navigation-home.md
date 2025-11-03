{% for link in site.data.navigation.main %}
  {% if link.right %}
    <a class="normal right" href="./{{ link.url }}">{{ link.title }}</a>
  {% else %}
    <!--<a class="normal" href="./{{ link.url }}">{{ link.title }}</a>-->
    <!-- Remy replace -->
    {% if link.title == 'Group' %}
      <a class="normal" href="{{ link.url }}">{{ link.title }}</a>
    {% else %}
      <a class="normal" href="../{{ link.url }}">{{ link.title }}</a>
    {% endif %}
  {% endif %}
{% endfor %}

