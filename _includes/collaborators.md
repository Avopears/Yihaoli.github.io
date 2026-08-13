<h2 id="research-collaborators">Research Collaborators</h2>

{% if site.data.collaborators.main and site.data.collaborators.main.size > 0 %}
<ul class="collaborator-list">
{% for collaborator in site.data.collaborators.main %}
  <li class="collaborator-card">
    <h3 class="collaborator-name">
      {% if collaborator.profile %}<a href="{{ collaborator.profile }}" target="_blank" rel="noopener noreferrer">{{ collaborator.name }}</a>{% elsif collaborator.website %}<a href="{{ collaborator.website }}" target="_blank" rel="noopener noreferrer">{{ collaborator.name }}</a>{% else %}{{ collaborator.name }}{% endif %}
    </h3>
    {% if collaborator.title %}<p class="collaborator-title">{{ collaborator.title }}</p>{% endif %}
    {% if collaborator.affiliations %}
    <ul class="collaborator-affiliations">
      {% for affiliation in collaborator.affiliations %}<li>{{ affiliation }}</li>{% endfor %}
    </ul>
    {% endif %}
    <div class="collaborator-links">
      {% if collaborator.email %}<a href="mailto:{{ collaborator.email }}" title="Email {{ collaborator.name }}"><i class="fa-regular fa-envelope" aria-hidden="true"></i> {{ collaborator.email }}</a>{% endif %}
      {% if collaborator.orcid %}<a href="https://orcid.org/{{ collaborator.orcid }}" target="_blank" rel="noopener noreferrer" title="{{ collaborator.name }} on ORCID"><i class="fa-brands fa-orcid" aria-hidden="true"></i> {{ collaborator.orcid }}</a>{% endif %}
      {% if collaborator.website %}<a href="{{ collaborator.website }}" target="_blank" rel="noopener noreferrer" title="Personal website of {{ collaborator.name }}"><i class="fa-solid fa-globe" aria-hidden="true"></i> Website</a>{% endif %}
    </div>
  </li>
{% endfor %}
</ul>
{% else %}
<p class="empty-state">Collaborator links will appear here after they are added to <code>_data/collaborators.yml</code>.</p>
{% endif %}
