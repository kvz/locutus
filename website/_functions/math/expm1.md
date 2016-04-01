---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/expm1/'
    original by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    improved by:
      - - 'Robert Eisele (http://www.xarg.org/)'
    note:
      - - "Precision 'n' can be adjusted as desired"
    example:
      - - expm1(1e-15);
    returns:
      - - '1.0000000000000007e-15'
function: expm1
category: math
permalink: /functions/expm1
redirect_from:
  - /functions/math/expm1/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function expm1 (x) {
  //  discuss at: http://phpjs.org/functions/expm1/
  // original by: Brett Zamir (http://brett-zamir.me)
  // improved by: Robert Eisele (http://www.xarg.org/)
  //        note: Precision 'n' can be adjusted as desired
  //   example 1: expm1(1e-15);
  //   returns 1: 1.0000000000000007e-15

  return (x < 1e-5 && -1e-5 < x) ? x + 0.5 * x * x : Math.exp(x) - 1
}

{% endhighlight %}

## Notes
- Precision 'n' can be adjusted as desired

## Example 1

{% highlight javascript %}
expm1(1e-15);
{% endhighlight %}

Should return

{% highlight javascript %}
expm1(1e-15);{% endhighlight %}


## Authors


Original by

- Brett Zamir (http://brett-zamir.me)


Improved by

- Robert Eisele (http://www.xarg.org/)
