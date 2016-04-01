---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/doubleval/'
    original by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    depends on:
      - - floatval
    note:
      - - '1.0 is simplified to 1 before it can be accessed by the function, this makes'
        - "it different from the PHP implementation. We can't fix this unfortunately."
    example:
      - - doubleval(186);
    returns:
      - - '186.00'
function: doubleval
category: var
permalink: /functions/doubleval
redirect_from:
  - /functions/var/doubleval/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function doubleval (mixed_var) {
  //  discuss at: http://phpjs.org/functions/doubleval/
  // original by: Brett Zamir (http://brett-zamir.me)
  //  depends on: floatval
  //        note: 1.0 is simplified to 1 before it can be accessed by the function, this makes
  //        note: it different from the PHP implementation. We can't fix this unfortunately.
  //   example 1: doubleval(186);
  //   returns 1: 186.00

  return this.floatval(mixed_var)
}

{% endhighlight %}

## Notes
- 1.0 is simplified to 1 before it can be accessed by the function, this makes,it different from the PHP implementation. We can't fix this unfortunately.

## Example 1

{% highlight javascript %}
doubleval(186);
{% endhighlight %}

Should return

{% highlight javascript %}
doubleval(186);{% endhighlight %}


## Authors


Original by

- Brett Zamir (http://brett-zamir.me)
