---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/is_float/'
    original by:
      - - Paulo Freitas
    bugfixed by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    improved by:
      - - 'WebDevHobo (http://webdevhobo.blogspot.com/)'
        - 'Rafał Kukawski (http://blog.kukawski.pl)'
    note:
      - - '1.0 is simplified to 1 before it can be accessed by the function, this makes'
        - "it different from the PHP implementation. We can't fix this unfortunately."
    example:
      - - is_float(186.31);
    returns:
      - - 'true'
function: is_float
category: var
permalink: /functions/is_float
redirect_from:
  - /functions/var/is_float/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function is_float (mixed_var) {
  //  discuss at: http://phpjs.org/functions/is_float/
  // original by: Paulo Freitas
  // bugfixed by: Brett Zamir (http://brett-zamir.me)
  // improved by: WebDevHobo (http://webdevhobo.blogspot.com/)
  // improved by: Rafał Kukawski (http://blog.kukawski.pl)
  //        note: 1.0 is simplified to 1 before it can be accessed by the function, this makes
  //        note: it different from the PHP implementation. We can't fix this unfortunately.
  //   example 1: is_float(186.31);
  //   returns 1: true

  return +mixed_var === mixed_var && (!isFinite(mixed_var) || !!(mixed_var % 1))
}

{% endhighlight %}

## Notes
- 1.0 is simplified to 1 before it can be accessed by the function, this makes,it different from the PHP implementation. We can't fix this unfortunately.

## Example 1

{% highlight javascript %}
is_float(186.31);
{% endhighlight %}

Should return

{% highlight javascript %}
is_float(186.31);{% endhighlight %}


## Authors


Original by

- Paulo Freitas


Improved by

- WebDevHobo (http://webdevhobo.blogspot.com/),Rafał Kukawski (http://blog.kukawski.pl)


Bugfixed by

- Brett Zamir (http://brett-zamir.me)
