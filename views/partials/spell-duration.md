{% if specificDuration == nil -%}
{{spellDuration}} {{durationUnit|map: 'DurationUnit'|l}}.

{% elif specificDuration == 'Concentration' -%}
{{specificDuration|map: 'SpellSpecificDuration'}}{% if spellDuration or durationUnit %}, {{'Spell.UpTo'|l}}{% endif %} {{spellDuration}} {{durationUnit|map: 'SpellDurationUnit'|l}}.

{% elif specificDuration == 'EffectDescription' -%}

{% if spellDuration or durationUnit %}{{spellDuration}} {{durationUnit|map: 'SpellDurationUnit'|l}} ;{% endif %} {{specificDuration|map: 'SpellSpecificDuration'}}.

{% else -%}
{{specialDuration|map: 'SpellDuration'}}
{% endif -%}