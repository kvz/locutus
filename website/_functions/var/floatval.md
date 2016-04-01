---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/floatval/'
    original by:
      - - 'Michael White (http://getsprink.com)'
    note:
      - - The native parseFloat() method of JavaScript returns NaN when it encounters a string before an int or float value.
    example:
      - - "floatval('150.03_page-section');"
      - - "floatval('page: 3');"
        - "floatval('-50 + 8');"
    returns:
      - - '150.03'
      - - '0'
        - '-50'
function: floatval
category: var
permalink: /functions/floatval
redirect_from:
  - /functions/var/floatval/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function floatval (mixed_var) {
  //  discuss at: http://phpjs.org/functions/floatval/
  // original by: Michael White (http://getsprink.com)
  //        note: The native parseFloat() method of JavaScript returns NaN when it encounters a string before an int or float value.
  //   example 1: floatval('150.03_page-section');
  //   returns 1: 150.03
  //   example 2: floatval('page: 3');
  //   example 2: floatval('-50 + 8');
  //   returns 2: 0
  //   returns 2: -50

  return (parseFloat(mixed_var) || 0)
}

{% endhighlight %}

## Notes
- The native parseFloat() method of JavaScript returns NaN when it encounters a string before an int or float value.

## Example 1

{% highlight javascript %}
floatval('150.03_page-section');
{% endhighlight %}

Should return

{% highlight javascript %}
floatval('150.03_page-section');{% endhighlight %}

## Example 2

{% highlight javascript %}
floatval('page: 3');,floatval('-50 + 8');
{% endhighlight %}

Should return

{% highlight javascript %}
floatval('page: 3');,floatval('-50 + 8');{% endhighlight %}


## Authors


Original by

- Michael White (http://getsprink.com)
