<!-- TITLE AND DEFINITION starts -->

{% assign title = "Time Frame" %}
{% assign definition = site.data.trading_system.time_frame %}
{% assign preposition = "a" %}

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

In the context of backtesting sessions, what time frame you decide to run the session on depends on the strategies being tested. If strategies make decisions based on the 1 hour candle and above, then ```01-hs``` may be the best choice. However, if decisions are influenced by sub-hour candles then you should match the time frame accordingly.

In the context of live sessions, that is, paper trading, forward testing and live trading, you should run the session on the ```01-min``` time frame so that the trading bot reacts fast when the price tags the take profit or stop loss targets.

<!-- CONTENT ends -->

{% endif %}

{% if include.adding != "" %}

{{include.adding}} Adding {{preposition}} {{title}}

<!-- ADDING starts -->

To add a parameter that may be missing, select *Add Missing Params* on the parameters node menu. 

<!-- ADDING ends -->

{% endif %}

{% if include.configuring != "" %}

{{include.adding}} Configuring the {{title}}

<!-- CONFIGURING starts -->

Select *Configure Time Frame* on the menu to access the configuration.

```js
{
"value": "01-min"
}
```

* ```value``` is the setting for the time frame. You may use any of the values below.

Available options at the sub-hour level are:

```json
01-min
02-min
03-min
04-min
05-min
10-min
15-min
20-min
30-min
45-min
```

Available options at larger time frames are:

```json
01-hs
02-hs
03-hs
04-hs
06-hs
08-hs
12-hs
24-hs
```

<!-- CONFIGURING ends -->

{% endif %}

