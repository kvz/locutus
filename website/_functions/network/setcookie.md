---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/setcookie/'
    original by:
      - - 'Jonas Raoni Soares Silva (http://www.jsfromhell.com)'
    bugfixed by:
      - - Andreas
        - Onno Marsman
    improved by:
      - - 'Kevin van Zonneveld (http://kevin.vanzonneveld.net)'
    depends on:
      - - setrawcookie
    example:
      - - "setcookie('author_name', 'Kevin van Zonneveld');"
    returns:
      - - 'true'
function: setcookie
category: network
permalink: /functions/setcookie
redirect_from:
  - /functions/network/setcookie/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function setcookie (name, value, expires, path, domain, secure) {
  //  discuss at: http://phpjs.org/functions/setcookie/
  // original by: Jonas Raoni Soares Silva (http://www.jsfromhell.com)
  // bugfixed by: Andreas
  // bugfixed by: Onno Marsman
  // improved by: Kevin van Zonneveld (http://kevin.vanzonneveld.net)
  //  depends on: setrawcookie
  //   example 1: setcookie('author_name', 'Kevin van Zonneveld');
  //   returns 1: true

  return this.setrawcookie(name, encodeURIComponent(value), expires, path, domain, secure)
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
setcookie('author_name', 'Kevin van Zonneveld');
{% endhighlight %}

Should return

{% highlight javascript %}
setcookie('author_name', 'Kevin van Zonneveld');{% endhighlight %}


## Authors


Original by

- Jonas Raoni Soares Silva (http://www.jsfromhell.com)


Improved by

- Kevin van Zonneveld (http://kevin.vanzonneveld.net)


Bugfixed by

- Andreas,Onno Marsman
