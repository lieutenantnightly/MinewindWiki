{% if item.image is defined %}

<figure markdown="span">
  ![{{ item["name"] }}](site:assets/{{ item["image"] }}){ width="300" }
</figure>

{% endif %}

Title: {{ item["name"] }}


Item Type: {{ item["item_type"] }}

{% if item.key_origin is defined %}
  Key Origin: {{ item["key_origin"] }}
{% endif %}

{% if item.soul_generates is defined %}
  Souls: {{ item["soul_generates"]["type"] }} {{ item["soul_generates"]["count"] }}
{% endif %}

{% if item.belphegors_blessing is defined %}
  Belphegors Blessing: {{ item["belphegors_blessing"]["type"] }} {{ item["belphegors_blessing"]["count"] }}
{% endif %}

{% if item.kill_counter is defined %}
  Has Kill Counter
{% endif %}

{% if item.soul_bound is defined %}
  Soul Bound: {{ item["soul_bound"] }}
{% endif %}

{% if item.lore is defined %}
  Lore:
  {% for line in item["lore"] %}
    {{ line }}
  {% endfor %}
{% endif %}

{% if item.date is defined %}
  Date: {{ item["date"] }}
{% endif %}

{% if item.worn_effects is defined %}
{% for worn_effect in item["worn_effects"] %}
{{ worn_effect["name"] }}
{% for effect in worn_effect["effects"] %}
- {{ effect }}
{% endfor %}
{% endfor %}
{% endif %}

{% if item.enchantments is defined %}

Enchantments:

| **Enchantment**                                    | **Level**           | **Hidden** | **Notes**           |
| :------------------------------------------------- | ------------------- | ------------------- | -- |
| {% for enchantment in item["enchantments"] %} {{ enchantment["name"] }} | {% if enchantment.level is defined %} {{ enchantment["level"] }} {% endif %} | {% if enchantment.hidden is defined %} :white_check_mark: {% endif %} | {% if enchantment.note is defined %} {{ enchantment["note"] }} {% endif %}
{% endfor %}
{% endif %}

{% if item.essences is defined %}

Essences:

| **Essence**                                    | **Level**           | **Locked** | **Notes**           |
| :------------------------------------------------- | ------------------- | ------------------- | -- |
| {% for essence in item["essences"] %} {{ essence["name"] }} | {% if essence.level is defined %} {{ essence["level"] }} {% endif %} | {% if essence.locked is defined %} :white_check_mark: {% endif %} | {% if essence.note is defined %} {{ essence["note"] }} {% endif %}
{% endfor %}
{% endif %}