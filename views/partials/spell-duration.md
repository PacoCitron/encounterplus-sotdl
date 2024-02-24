{% if specialDuration == nil -%}
{{spellDuration}} {{durationUnit|map: 'SpellDurationUnit'|l}}

{% elif specialDuration == 'Concentration' -%}
{{specialDuration|map: 'SpellSpecialDuration'}}{% if spellDuration or durationUnit %}, {{'Spell.UpTo'|l}}{% endif %} {{spellDuration}} {{durationUnit|map: 'SpellDurationUnit'|l}}

{% elif specialDuration == 'EffectDescription' -%}

{% if spellDuration or durationUnit %} {{spellDuration}} {{durationUnit|map: 'SpellDurationUnit'|l}}{% endif %} ; {{specialDuration|map: 'SpellSpecialDuration'}}

{% else -%}
{{specialDuration|map: 'SpellDuration'}}
{% endif -%}  