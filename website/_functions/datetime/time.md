---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/time/'
    original by:
      - - 'GeekFG (http://geekfg.blogspot.com)'
    improved by:
      - - 'Kevin van Zonneveld (http://kevin.vanzonneveld.net)'
        - metjay
        - HKM
    example:
      - - timeStamp = time();
        - 'timeStamp > 1000000000 && timeStamp < 2000000000'
    returns:
      - - 'true'
function: time
category: datetime
permalink: /functions/time
redirect_from:
  - /functions/datetime/time/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function time () {
  //  discuss at: http://phpjs.org/functions/time/
  // original by: GeekFG (http://geekfg.blogspot.com)
  // improved by: Kevin van Zonneveld (http://kevin.vanzonneveld.net)
  // improved by: metjay
  // improved by: HKM
  //   example 1: timeStamp = time();
  //   example 1: timeStamp > 1000000000 && timeStamp < 2000000000
  //   returns 1: true

  return Math.floor(new Date()
    .getTime() / 1000)
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
timeStamp = time();,timeStamp > 1000000000 && timeStamp < 2000000000
{% endhighlight %}

Should return

{% highlight javascript %}
timeStamp = time();,timeStamp > 1000000000 && timeStamp < 2000000000{% endhighlight %}


## Authors


Original by

- GeekFG (http://geekfg.blogspot.com)


Improved by

- Kevin van Zonneveld (http://kevin.vanzonneveld.net),metjay,HKM
