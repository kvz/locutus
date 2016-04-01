---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/stripslashes/'
    original by:
      - - 'Kevin van Zonneveld (http://kevin.vanzonneveld.net)'
    improved by:
      - - 'Ates Goral (http://magnetiq.com)'
        - marrtins
        - rezna
    fixed by:
      - - Mick@el
    bugfixed by:
      - - Onno Marsman
        - 'Brett Zamir (http://brett-zamir.me)'
    input by:
      - - Rick Waldron
        - 'Brant Messenger (http://www.brantmessenger.com/)'
    reimplemented by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    example:
      - - "stripslashes('Kevin\\'s code');"
      - - "stripslashes('Kevin\\\\\\'s code');"
    returns:
      - - "\"Kevin's code\""
      - - "\"Kevin\\'s code\""
function: stripslashes
category: strings
permalink: /functions/stripslashes
redirect_from:
  - /functions/strings/stripslashes/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function stripslashes (str) {
  //       discuss at: http://phpjs.org/functions/stripslashes/
  //      original by: Kevin van Zonneveld (http://kevin.vanzonneveld.net)
  //      improved by: Ates Goral (http://magnetiq.com)
  //      improved by: marrtins
  //      improved by: rezna
  //         fixed by: Mick@el
  //      bugfixed by: Onno Marsman
  //      bugfixed by: Brett Zamir (http://brett-zamir.me)
  //         input by: Rick Waldron
  //         input by: Brant Messenger (http://www.brantmessenger.com/)
  // reimplemented by: Brett Zamir (http://brett-zamir.me)
  //        example 1: stripslashes('Kevin\'s code');
  //        returns 1: "Kevin's code"
  //        example 2: stripslashes('Kevin\\\'s code');
  //        returns 2: "Kevin\'s code"

  return (str + '')
    .replace(/\\(.?)/g, function (s, n1) {
      switch (n1) {
        case '\\':
          return '\\'
        case '0':
          return '\u0000'
        case '':
          return ''
        default:
          return n1
      }
    })
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
stripslashes('Kevin\'s code');
{% endhighlight %}

Should return

{% highlight javascript %}
stripslashes('Kevin\'s code');{% endhighlight %}

## Example 2

{% highlight javascript %}
stripslashes('Kevin\\\'s code');
{% endhighlight %}

Should return

{% highlight javascript %}
stripslashes('Kevin\\\'s code');{% endhighlight %}


## Authors


Original by

- Kevin van Zonneveld (http://kevin.vanzonneveld.net)


Improved by

- Ates Goral (http://magnetiq.com),marrtins,rezna


Bugfixed by

- Onno Marsman,Brett Zamir (http://brett-zamir.me)


Input by

- Rick Waldron,Brant Messenger (http://www.brantmessenger.com/)
