---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/gettype/'
    original by:
      - - Paulo Freitas
    improved by:
      - - 'Kevin van Zonneveld (http://kevin.vanzonneveld.net)'
        - 'Douglas Crockford (http://javascript.crockford.com)'
        - 'Brett Zamir (http://brett-zamir.me)'
    input by:
      - - KELAN
    depends on:
      - - is_float
    note:
      - - '1.0 is simplified to 1 before it can be accessed by the function, this makes'
        - "it different from the PHP implementation. We can't fix this unfortunately."
    example:
      - - gettype(1);
      - - gettype(undefined);
      - - "gettype({0: 'Kevin van Zonneveld'});"
      - - "gettype('foo');"
      - - 'gettype({0: function () {return false;}});'
      - - "gettype({0: 'test', length: 1, splice: function () {}});"
        - "gettype(['test']);"
    returns:
      - - "'integer'"
      - - "'undefined'"
      - - "'object'"
      - - "'string'"
      - - "'object'"
      - - "'object'"
        - "'array'"
function: gettype
category: var
permalink: /functions/gettype
redirect_from:
  - /functions/var/gettype/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function gettype (mixed_var) {
  //  discuss at: http://phpjs.org/functions/gettype/
  // original by: Paulo Freitas
  // improved by: Kevin van Zonneveld (http://kevin.vanzonneveld.net)
  // improved by: Douglas Crockford (http://javascript.crockford.com)
  // improved by: Brett Zamir (http://brett-zamir.me)
  //    input by: KELAN
  //  depends on: is_float
  //        note: 1.0 is simplified to 1 before it can be accessed by the function, this makes
  //        note: it different from the PHP implementation. We can't fix this unfortunately.
  //   example 1: gettype(1);
  //   returns 1: 'integer'
  //   example 2: gettype(undefined);
  //   returns 2: 'undefined'
  //   example 3: gettype({0: 'Kevin van Zonneveld'});
  //   returns 3: 'object'
  //   example 4: gettype('foo');
  //   returns 4: 'string'
  //   example 5: gettype({0: function () {return false;}});
  //   returns 5: 'object'
  //   example 6: gettype({0: 'test', length: 1, splice: function () {}});
  //   example 6: gettype(['test']);
  //   returns 6: 'object'
  //   returns 6: 'array'

  var s = typeof mixed_var,
    name
  var getFuncName = function (fn) {
    var name = (/\W*function\s+([\w\$]+)\s*\(/)
      .exec(fn)
    if (!name) {
      return '(Anonymous)'
    }
    return name[1]
  }
  if (s === 'object') {
    if (mixed_var !== null) {
      // From: http://javascript.crockford.com/remedial.html
      if (typeof mixed_var.length === 'number' && !(mixed_var.propertyIsEnumerable('length')) && typeof mixed_var
        .splice === 'function') {
        s = 'array'
      } else if (mixed_var.constructor && getFuncName(mixed_var.constructor)) {
        name = getFuncName(mixed_var.constructor)
        if (name === 'Date') {
          // not in PHP
          s = 'date'
        } else if (name === 'RegExp') {
          // not in PHP
          s = 'regexp'
        } else if (name === 'PHPJS_Resource') {
          // Check against our own resource constructor
          s = 'resource'
        }
      }
    } else {
      s = 'null'
    }
  } else if (s === 'number') {
    s = this.is_float(mixed_var) ? 'double' : 'integer'
  }
  return s
}

{% endhighlight %}

## Notes
- 1.0 is simplified to 1 before it can be accessed by the function, this makes,it different from the PHP implementation. We can't fix this unfortunately.

## Example 1

{% highlight javascript %}
gettype(1);
{% endhighlight %}

Should return

{% highlight javascript %}
gettype(1);{% endhighlight %}

## Example 2

{% highlight javascript %}
gettype(undefined);
{% endhighlight %}

Should return

{% highlight javascript %}
gettype(undefined);{% endhighlight %}

## Example 3

{% highlight javascript %}
gettype({0: 'Kevin van Zonneveld'});
{% endhighlight %}

Should return

{% highlight javascript %}
gettype({0: 'Kevin van Zonneveld'});{% endhighlight %}

## Example 4

{% highlight javascript %}
gettype('foo');
{% endhighlight %}

Should return

{% highlight javascript %}
gettype('foo');{% endhighlight %}

## Example 5

{% highlight javascript %}
gettype({0: function () {return false;}});
{% endhighlight %}

Should return

{% highlight javascript %}
gettype({0: function () {return false;}});{% endhighlight %}

## Example 6

{% highlight javascript %}
gettype({0: 'test', length: 1, splice: function () {}});,gettype(['test']);
{% endhighlight %}

Should return

{% highlight javascript %}
gettype({0: 'test', length: 1, splice: function () {}});,gettype(['test']);{% endhighlight %}


## Authors


Original by

- Paulo Freitas


Improved by

- Kevin van Zonneveld (http://kevin.vanzonneveld.net),Douglas Crockford (http://javascript.crockford.com),Brett Zamir (http://brett-zamir.me)


Input by

- KELAN
