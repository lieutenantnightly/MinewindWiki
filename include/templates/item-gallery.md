{% if item.additional_images is defined %}
{% for image in item["additional_images"] %}
{% if image.description is defined %}

<figure markdown="span">
  ![{{ image["description"] }}](site:assets/{{ image["path"] }}){ data-description="{{ image["description"] }}" width="300" }
  <figcaption>{{ image["description"] }}</figcaption>
</figure>

{% else %}

<figure markdown="span">
  ![{{ item["name"] }}](site:assets/{{ image["path"] }}){ width="300" }
</figure>

{% endif %}
{% endfor %}

{% else %}

No more images are available.

{% endif %}