<h2 id="research-collaborators">Research Collaborators</h2>

{% if site.data.collaborators.main and site.data.collaborators.main.size > 0 %}
<ul class="collaborator-list">
{% for collaborator in site.data.collaborators.main %}
  <li>
    <a href="{{ collaborator.url }}"><strong>{{ collaborator.name }}</strong></a>
    {% if collaborator.affiliation %}<span> — {{ collaborator.affiliation }}</span>{% endif %}
  </li>
{% endfor %}
</ul>
{% else %}
<p class="empty-state">Collaborator links will appear here after they are added to <code>_data/collaborators.yml</code>.</p>
{% endif %}

