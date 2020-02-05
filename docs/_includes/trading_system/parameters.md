<!-- TITLE AND DEFINITION starts -->

{% assign title = "Parameters" %}
{% assign definition = site.data.trading_system.parameters %}
{% assign preposition = "" %}

<!-- TITLE AND DEFINITION ends -->

{% if include.heading != "" %}
{{include.heading}} {{title}}
{% endif %}

{% if include.icon != "no" %} 

{% if include.table == "y" %}
<table class="definitionTable"><tr><td>
{% endif %}

<img src='images/icons/{{include.icon}}{{ title | downcase | replace: " ", "-" }}.png' />

{% if include.table == "y" %}
</td><td>
{% endif %}

{% endif %}

{% if include.definition != "regular" %}

<strong>{{ definition }}</strong>

{% else %}

{{ definition }}

{% endif %}

{% if include.table == "y" and include.icon != "no" %}
</td></tr></table>
{% endif %}

{% if include.content != "n" %}

<!-- CONTENT starts -->

Each testing session has its own set of parameters. This allows you to configure different trading sessions with different parameters, and go back and forth between them as required. For instance, you may have different backtesting sessions with different date ranges, different exchange fees or different slippage settings.

<!-- CONTENT ends -->

{% endif %}

{% if include.adding != "" %}

{{include.adding}} Adding {{preposition}} {{title}}

<!-- ADDING starts -->

To add a parameters node, select *Add Parameters* on the session or the trading system menu, depending on the context. When a parameters node is added, the full set of parameters are created with it.

If you already have a parameters node but are missing some of the parameters, then select *Add Missing Params* on the menu.

<!-- ADDING ends -->

{% endif %}

{% if include.configuring != "" %}

{{include.configuring}} Configuring the {{title}}

<!-- CONFIGURING starts -->

XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

<!-- CONFIGURING ends -->

{% endif %}

