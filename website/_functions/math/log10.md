---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/log10/'
    original by:
      - - Philip Peterson
    improved by:
      - - Onno Marsman
        - Tod Gentille
        - 'Brett Zamir (http://brett-zamir.me)'
    example:
      - - log10(10);
      - - log10(1);
    returns:
      - - '1'
      - - '0'
function: log10
category: math
permalink: /functions/log10
redirect_from:
  - /functions/math/log10/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function log10 (arg) {
  //  discuss at: http://phpjs.org/functions/log10/
  // original by: Philip Peterson
  // improved by: Onno Marsman
  // improved by: Tod Gentille
  // improved by: Brett Zamir (http://brett-zamir.me)
  //   example 1: log10(10);
  //   returns 1: 1
  //   example 2: log10(1);
  //   returns 2: 0

  return Math.log(arg) / 2.302585092994046 // Math.LN10
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
log10(10);
{% endhighlight %}

Should return

{% highlight javascript %}
log10(10);{% endhighlight %}

## Example 2

{% highlight javascript %}
log10(1);
{% endhighlight %}

Should return

{% highlight javascript %}
log10(1);{% endhighlight %}


## Authors


Original by

- Philip Peterson


Improved by

- Onno Marsman,Tod Gentille,Brett Zamir (http://brett-zamir.me)
