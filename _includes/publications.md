<h2 id="research-articles">Research Articles (as First<sup>#</sup> &amp; Corresponding<sup>*</sup> Author)</h2>

{% if site.data.publications.main and site.data.publications.main.size > 0 %}
<div class="publications">
  <ol class="bibliography">
  {% for publication in site.data.publications.main %}
    <li>
      <article class="pub-row">
        {% if publication.image %}
        <div class="pub-media">
          <img src="{{ publication.image | relative_url }}" alt="Thumbnail for {{ publication.title }}" loading="lazy">
          {% if publication.conference_short %}<span class="pub-badge">{{ publication.conference_short }}</span>{% endif %}
        </div>
        {% endif %}
        <div class="pub-content">
          <h3 class="pub-title">
            {% if publication.number %}<span class="pub-number">{{ publication.number }}.</span>{% endif %}
            {% if publication.page %}<a href="{{ publication.page }}">{{ publication.title }}</a>{% else %}{{ publication.title }}{% endif %}
          </h3>
          <p class="pub-authors">{{ publication.authors }}</p>
          <p class="pub-venue"><em>{{ publication.conference }}</em></p>
          <div class="pub-links">
            {% if publication.pdf %}
              {% if publication.pdf contains '://' %}<a href="{{ publication.pdf }}">PDF</a>{% else %}<a href="{{ publication.pdf | relative_url }}">PDF</a>{% endif %}
            {% endif %}
            {% if publication.code %}<a href="{{ publication.code }}">Code</a>{% endif %}
            {% if publication.page %}<a href="{{ publication.page }}">Article Website</a>{% endif %}
            {% if publication.bibtex %}<a href="{{ publication.bibtex | relative_url }}">BibTeX</a>{% endif %}
            {% if publication.notes %}<strong>{{ publication.notes }}</strong>{% endif %}
          </div>
        </div>
      </article>
    </li>
  {% endfor %}
  </ol>
</div>
{% else %}
<p class="empty-state">Publication entries will appear here after they are added to <code>_data/publications.yml</code>.</p>
{% endif %}
