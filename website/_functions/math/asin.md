---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/asin/'
    original by:
      - - Onno Marsman
    note:
      - - Sorry about the crippled test. Needed because precision differs accross platforms.
    example:
      - - "(asin(0.3) + '').substr(0, 17);"
    returns:
      - - '"0.304692654015397"'
function: asin
category: math
permalink: /functions/asin
redirect_from:
  - /functions/math/asin/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function asin (arg) {
  //  discuss at: http://phpjs.org/functions/asin/
  // original by: Onno Marsman
  //        note: Sorry about the crippled test. Needed because precision differs accross platforms.
  //   example 1: (asin(0.3) + '').substr(0, 17);
  //   returns 1: "0.304692654015397"

  return Math.asin(arg)
}

{% endhighlight %}

## Notes
- Sorry about the crippled test. Needed because precision differs accross platforms.

## Example 1

{% highlight javascript %}
(asin(0.3) + '').substr(0, 17);
{% endhighlight %}

Should return

{% highlight javascript %}
(asin(0.3) + '').substr(0, 17);{% endhighlight %}


## Authors


Original by

- Onno Marsman
