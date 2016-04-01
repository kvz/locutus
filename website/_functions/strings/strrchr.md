---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/strrchr/'
    original by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    input by:
      - - 'Jason Wong (http://carrot.org/)'
    bugfixed by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    example:
      - - "strrchr(\"Line 1\\nLine 2\\nLine 3\", 10).substr(1)"
    returns:
      - - "'Line 3'"
function: strrchr
category: strings
permalink: /functions/strrchr
redirect_from:
  - /functions/strings/strrchr/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function strrchr (haystack, needle) {
  //  discuss at: http://phpjs.org/functions/strrchr/
  // original by: Brett Zamir (http://brett-zamir.me)
  //    input by: Jason Wong (http://carrot.org/)
  // bugfixed by: Brett Zamir (http://brett-zamir.me)
  //   example 1: strrchr("Line 1\nLine 2\nLine 3", 10).substr(1)
  //   returns 1: 'Line 3'

  var pos = 0

  if (typeof needle !== 'string') {
    needle = String.fromCharCode(parseInt(needle, 10))
  }
  needle = needle.charAt(0)
  pos = haystack.lastIndexOf(needle)
  if (pos === -1) {
    return false
  }

  return haystack.substr(pos)
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
strrchr("Line 1\nLine 2\nLine 3", 10).substr(1)
{% endhighlight %}

Should return

{% highlight javascript %}
strrchr("Line 1\nLine 2\nLine 3", 10).substr(1){% endhighlight %}


## Authors


Original by

- Brett Zamir (http://brett-zamir.me)


Bugfixed by

- Brett Zamir (http://brett-zamir.me)


Input by

- Jason Wong (http://carrot.org/)
