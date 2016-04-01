---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/set_time_limit/'
    original by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    test:
      - - skip
    example:
      - - set_time_limit(4);
    returns:
      - - undefined
function: set_time_limit
category: info
permalink: /functions/set_time_limit
redirect_from:
  - /functions/info/set_time_limit/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function set_time_limit (seconds) {
  //  discuss at: http://phpjs.org/functions/set_time_limit/
  // original by: Brett Zamir (http://brett-zamir.me)
  //        test: skip
  //   example 1: set_time_limit(4);
  //   returns 1: undefined

  // BEGIN REDUNDANT
  this.php_js = this.php_js || {}
  // END REDUNDANT

  this.window.setTimeout(function () {
    if (!this.php_js.timeoutStatus) {
      this.php_js.timeoutStatus = true
    }
    throw 'Maximum execution time exceeded'
  }, seconds * 1000)
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
set_time_limit(4);
{% endhighlight %}

Should return

{% highlight javascript %}
set_time_limit(4);{% endhighlight %}


## Authors


Original by

- Brett Zamir (http://brett-zamir.me)
