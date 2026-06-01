<table class="publication-table"><tbody>
{% for paper in site.data.publications.main %}
  <tr{% if paper.highlight %} class="highlight-row"{% endif %}>
    <td class="paper-image-cell">
      {% if paper.video_group %}
      <div class="paper-image paper-image-placeholder"></div>
      {% elsif paper.image %}
      <img src="{{ paper.image }}" class="paper-image" alt="{{ paper.title }}">
      {% endif %}
    </td>
    <td class="paper-copy-cell">
      {% if paper.page %}
      <a href="{{ paper.page }}"><span class="papertitle">{{ paper.title }}</span></a>
      {% elsif paper.pdf %}
      <a href="{{ paper.pdf }}"><span class="papertitle">{{ paper.title }}</span></a>
      {% else %}
      <span class="papertitle">{{ paper.title }}</span>
      {% endif %}
      <br>
      <span class="authors">{{ paper.authors }}</span>
      <br>
      <em>{{ paper.conference }}</em>
      {% if paper.notes %}
      &nbsp;<span class="note">{{ paper.notes }}</span>
      {% endif %}
      <br>
      <span class="paper-links">
        {% if paper.page %}<a href="{{ paper.page }}">project page</a>{% endif %}
        {% if paper.page and paper.pdf %} / {% endif %}
        {% if paper.pdf %}<a href="{{ paper.pdf }}">paper</a>{% endif %}
        {% if paper.code %}
        {% if paper.page or paper.pdf %} / {% endif %}
        <a href="{{ paper.code }}">code</a>
        {% endif %}
      </span>
      {% if paper.summary %}
      <p>{{ paper.summary }}</p>
      {% endif %}
    </td>
  </tr>
{% endfor %}
</tbody></table>
