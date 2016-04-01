---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/strcmp/'
    original by:
      - - 'Waldo Malqui Silva (http://waldo.malqui.info)'
    input by:
      - - Steve Hilder
    improved by:
      - - 'Kevin van Zonneveld (http://kevin.vanzonneveld.net)'
    revised by:
      - - gorthaur
    example:
      - - "strcmp( 'waldo', 'owald' );"
      - - "strcmp( 'owald', 'waldo' );"
    returns:
      - - '1'
      - - '-1'
function: strcmp
category: strings
permalink: /functions/strcmp
redirect_from:
  - /functions/strings/strcmp/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function strcmp (str1, str2) {
  //  discuss at: http://phpjs.org/functions/strcmp/
  // original by: Waldo Malqui Silva (http://waldo.malqui.info)
  //    input by: Steve Hilder
  // improved by: Kevin van Zonneveld (http://kevin.vanzonneveld.net)
  //  revised by: gorthaur
  //   example 1: strcmp( 'waldo', 'owald' );
  //   returns 1: 1
  //   example 2: strcmp( 'owald', 'waldo' );
  //   returns 2: -1

  return ((str1 == str2) ? 0 : ((str1 > str2) ? 1 : -1))
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
strcmp( 'waldo', 'owald' );
{% endhighlight %}

Should return

{% highlight javascript %}
strcmp( 'waldo', 'owald' );{% endhighlight %}

## Example 2

{% highlight javascript %}
strcmp( 'owald', 'waldo' );
{% endhighlight %}

Should return

{% highlight javascript %}
strcmp( 'owald', 'waldo' );{% endhighlight %}


## Authors


Original by

- Waldo Malqui Silva (http://waldo.malqui.info)


Improved by

- Kevin van Zonneveld (http://kevin.vanzonneveld.net)


Revised by

- gorthaur


Input by

- Steve Hilder
