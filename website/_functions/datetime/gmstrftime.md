---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/gmstrftime/'
    original by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    input by:
      - - Alex
    bugfixed by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    depends on:
      - - strftime
    example:
      - - 'gmstrftime("%A", 1062462400);'
    returns:
      - - "'Tuesday'"
function: gmstrftime
category: datetime
permalink: /functions/gmstrftime
redirect_from:
  - /functions/datetime/gmstrftime/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function gmstrftime (format, timestamp) {
  //  discuss at: http://phpjs.org/functions/gmstrftime/
  // original by: Brett Zamir (http://brett-zamir.me)
  //    input by: Alex
  // bugfixed by: Brett Zamir (http://brett-zamir.me)
  //  depends on: strftime
  //   example 1: gmstrftime("%A", 1062462400);
  //   returns 1: 'Tuesday'

  var dt = ((typeof timestamp === 'undefined') ? new Date() : // Not provided
    (typeof timestamp === 'object') ? new Date(timestamp) : // Javascript Date()
    new Date(timestamp * 1000) // UNIX timestamp (auto-convert to int)
  )
  timestamp = Date.parse(dt.toUTCString()
    .slice(0, -4)) / 1000
  return this.strftime(format, timestamp)
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
gmstrftime("%A", 1062462400);
{% endhighlight %}

Should return

{% highlight javascript %}
gmstrftime("%A", 1062462400);{% endhighlight %}


## Authors


Original by

- Brett Zamir (http://brett-zamir.me)


Bugfixed by

- Brett Zamir (http://brett-zamir.me)


Input by

- Alex
