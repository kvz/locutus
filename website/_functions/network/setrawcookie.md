---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/setrawcookie/'
    original by:
      - - 'Brett Zamir (http://brett-zamir.me)'
        - setcookie
    improved by:
      - - 'Kevin van Zonneveld (http://kevin.vanzonneveld.net)'
    input by:
      - - Michael
    bugfixed by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    example:
      - - "setrawcookie('author_name', 'Kevin van Zonneveld');"
    returns:
      - - 'true'
function: setrawcookie
category: network
permalink: /functions/setrawcookie
redirect_from:
  - /functions/network/setrawcookie/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function setrawcookie (name, value, expires, path, domain, secure) {
  //  discuss at: http://phpjs.org/functions/setrawcookie/
  // original by: Brett Zamir (http://brett-zamir.me)
  // original by: setcookie
  // improved by: Kevin van Zonneveld (http://kevin.vanzonneveld.net)
  //    input by: Michael
  // bugfixed by: Brett Zamir (http://brett-zamir.me)
  //   example 1: setrawcookie('author_name', 'Kevin van Zonneveld');
  //   returns 1: true

  if (typeof expires === 'string' && (/^\d+$/)
    .test(expires)) {
    expires = parseInt(expires, 10)
  }

  if (expires instanceof Date) {
    expires = expires.toUTCString()
  } else if (typeof expires === 'number') {
    expires = (new Date(expires * 1e3))
      .toUTCString()
  }

  var r = [name + '=' + value],
    s = {},
    i = ''
  s = {
    expires: expires,
    path: path,
    domain: domain
  }
  for (i in s) {
    if (s.hasOwnProperty(i)) {
      // Exclude items on Object.prototype
      s[i] && r.push(i + '=' + s[i])
    }
  }

  return secure && r.push('secure'), this.window.document.cookie = r.join(';'), true
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
setrawcookie('author_name', 'Kevin van Zonneveld');
{% endhighlight %}

Should return

{% highlight javascript %}
setrawcookie('author_name', 'Kevin van Zonneveld');{% endhighlight %}


## Authors


Original by

- Brett Zamir (http://brett-zamir.me),setcookie


Improved by

- Kevin van Zonneveld (http://kevin.vanzonneveld.net)


Bugfixed by

- Brett Zamir (http://brett-zamir.me)


Input by

- Michael
