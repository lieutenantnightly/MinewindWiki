---
aliases:
  - builders-hat
---
# Builder's Hat

The Builder's Hat is a [[mythical]] Turtle helmet that was awarded to SliquifierC on his build of [[Spawn]].

{%
    set builders_hat = {
        "name": "Builder's Hat",
        "image": "builders-hat.webp",
        "item_type": "turtle_helmet",
        "enchantments": [
            {
                "name": "Protection",
                "level": "10",
            }, {
                "name": "Respiration",
                "level": "10",
            }, {
                "name": "Unbreaking",
                "level": "10",
            }, {
                "name": "Projectile Protection",
                "level": "10",
            }, {
                "name": "Aqua Affinity",
            }, {
                "name": "Blast Protection",
                "level": "10",
            }, {
                "name": "Fire Protection",
                "level": "10",
            }, {
                "name": "Soulbound",
            }, {
                "name": "Indestructible",
            }, {
                "name": "Undroppable",
            },
        ],
        "lore": [
            "Enchanted with the lifeforce",
            "of spectral turtle dragons.",
        ],
        "worn_effects": [{
            "name": "When on Head:",
            "effects": [
                "+2 Armor",
                "+10 Oxygen Bonus",
                "+400% Submerged Mining Speed"
            ]
        }, {
            "name": "When worn:",
            "effects": [
                "+1.5 Explosion Knockback Resistance",
                "-150% Burning Time",
            ]
        }],
        "soul_bound": "SliquifierC",
    }
%}

{% set item = builders_hat %}
{% include 'templates/item.md' %}