---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/long2ip/'
    original by:
      - - 'Waldo Malqui Silva (http://waldo.malqui.info)'
    example:
      - - long2ip( 3221234342 );
    returns:
      - - "'192.0.34.166'"
function: long2ip
category: network
permalink: /functions/long2ip
redirect_from:
  - /functions/network/long2ip/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function long2ip (ip) {
  //  discuss at: http://phpjs.org/functions/long2ip/
  // original by: Waldo Malqui Silva (http://waldo.malqui.info)
  //   example 1: long2ip( 3221234342 );
  //   returns 1: '192.0.34.166'

  if (!isFinite(ip))
    return false

  return [ip >>> 24, ip >>> 16 & 0xFF, ip >>> 8 & 0xFF, ip & 0xFF].join('.')
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
long2ip( 3221234342 );
{% endhighlight %}

Should return

{% highlight javascript %}
long2ip( 3221234342 );{% endhighlight %}


## Authors


Original by

- Waldo Malqui Silva (http://waldo.malqui.info)
