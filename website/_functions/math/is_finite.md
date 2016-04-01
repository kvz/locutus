---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/is_finite/'
    original by:
      - - Onno Marsman
    example:
      - - is_finite(Infinity);
      - - is_finite(-Infinity);
      - - is_finite(0);
    returns:
      - - 'false'
      - - 'false'
      - - 'true'
function: is_finite
category: math
permalink: /functions/is_finite
redirect_from:
  - /functions/math/is_finite/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function is_finite (val) {
  //  discuss at: http://phpjs.org/functions/is_finite/
  // original by: Onno Marsman
  //   example 1: is_finite(Infinity);
  //   returns 1: false
  //   example 2: is_finite(-Infinity);
  //   returns 2: false
  //   example 3: is_finite(0);
  //   returns 3: true

  var warningType = ''

  if (val === Infinity || val === -Infinity) {
    return false
  }

  // Some warnings for maximum PHP compatibility
  if (typeof val === 'object') {
    warningType = (Object.prototype.toString.call(val) === '[object Array]' ? 'array' : 'object')
  } else if (typeof val === 'string' && !val.match(/^[\+\-]?\d/)) {
    // simulate PHP's behaviour: '-9a' doesn't give a warning, but 'a9' does.
    warningType = 'string'
  }
  if (warningType) {
    throw new Error('Warning: is_finite() expects parameter 1 to be double, ' + warningType + ' given')
  }

  return true
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
is_finite(Infinity);
{% endhighlight %}

Should return

{% highlight javascript %}
is_finite(Infinity);{% endhighlight %}

## Example 2

{% highlight javascript %}
is_finite(-Infinity);
{% endhighlight %}

Should return

{% highlight javascript %}
is_finite(-Infinity);{% endhighlight %}

## Example 3

{% highlight javascript %}
is_finite(0);
{% endhighlight %}

Should return

{% highlight javascript %}
is_finite(0);{% endhighlight %}


## Authors


Original by

- Onno Marsman
