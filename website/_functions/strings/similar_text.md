---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/similar_text/'
    original by:
      - - 'Rafał Kukawski (http://blog.kukawski.pl)'
    bugfixed by:
      - - Chris McMacken
        - 'Jarkko Rantavuori original by findings in stackoverflow (http://stackoverflow.com/questions/14136349/how-does-similar-text-work)'
    improved by:
      - - 'Markus Padourek (taken from http://www.kevinhq.com/2012/06/php-similartext-function-in-javascript_16.html)'
    example:
      - - "similar_text('Hello World!', 'Hello phpjs!');"
      - - "similar_text('Hello World!', null);"
    returns:
      - - '7'
      - - '0'
function: similar_text
category: strings
permalink: /functions/similar_text
redirect_from:
  - /functions/strings/similar_text/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function similar_text (first, second, percent) {
  //  discuss at: http://phpjs.org/functions/similar_text/
  // original by: Rafał Kukawski (http://blog.kukawski.pl)
  // bugfixed by: Chris McMacken
  // bugfixed by: Jarkko Rantavuori original by findings in stackoverflow (http://stackoverflow.com/questions/14136349/how-does-similar-text-work)
  // improved by: Markus Padourek (taken from http://www.kevinhq.com/2012/06/php-similartext-function-in-javascript_16.html)
  //   example 1: similar_text('Hello World!', 'Hello phpjs!');
  //   returns 1: 7
  //   example 2: similar_text('Hello World!', null);
  //   returns 2: 0

  if (first === null || second === null || typeof first === 'undefined' || typeof second === 'undefined') {
    return 0
  }

  first += ''
  second += ''

  var pos1 = 0,
    pos2 = 0,
    max = 0,
    firstLength = first.length,
    secondLength = second.length,
    p, q, l, sum

  max = 0

  for (p = 0; p < firstLength; p++) {
    for (q = 0; q < secondLength; q++) {
      for (l = 0;
        (p + l < firstLength) && (q + l < secondLength) && (first.charAt(p + l) === second.charAt(q + l)); l++)
        ;
      if (l > max) {
        max = l
        pos1 = p
        pos2 = q
      }
    }
  }

  sum = max

  if (sum) {
    if (pos1 && pos2) {
      sum += this.similar_text(first.substr(0, pos1), second.substr(0, pos2))
    }

    if ((pos1 + max < firstLength) && (pos2 + max < secondLength)) {
      sum += this.similar_text(first.substr(pos1 + max, firstLength - pos1 - max), second.substr(pos2 + max,
        secondLength - pos2 - max))
    }
  }

  if (!percent) {
    return sum
  } else {
    return (sum * 200) / (firstLength + secondLength)
  }
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
similar_text('Hello World!', 'Hello phpjs!');
{% endhighlight %}

Should return

{% highlight javascript %}
similar_text('Hello World!', 'Hello phpjs!');{% endhighlight %}

## Example 2

{% highlight javascript %}
similar_text('Hello World!', null);
{% endhighlight %}

Should return

{% highlight javascript %}
similar_text('Hello World!', null);{% endhighlight %}


## Authors


Original by

- Rafał Kukawski (http://blog.kukawski.pl)


Improved by

- Markus Padourek (taken from http://www.kevinhq.com/2012/06/php-similartext-function-in-javascript_16.html)


Bugfixed by

- Chris McMacken,Jarkko Rantavuori original by findings in stackoverflow (http://stackoverflow.com/questions/14136349/how-does-similar-text-work)
