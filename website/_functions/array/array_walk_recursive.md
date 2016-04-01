---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/array_walk_recursive/'
    original by:
      - - 'Johnny Mast (http://www.phpvrouwen.nl)'
    example:
      - - "array_walk_recursive ({'a': 'b', 'c': {'d': 'e'}}, 'void', 'userdata');"
      - - "array_walk_recursive ('a', 'void', 'userdata');"
    returns:
      - - 'true'
      - - 'false'
function: array_walk_recursive
category: array
permalink: /functions/array_walk_recursive
redirect_from:
  - /functions/array/array_walk_recursive/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function array_walk_recursive (array, funcname, userdata) {
  //  discuss at: http://phpjs.org/functions/array_walk_recursive/
  // original by: Johnny Mast (http://www.phpvrouwen.nl)
  //   example 1: array_walk_recursive ({'a': 'b', 'c': {'d': 'e'}}, 'void', 'userdata');
  //   returns 1: true
  //   example 2: array_walk_recursive ('a', 'void', 'userdata');
  //   returns 2: false

  var key

  if (typeof array !== 'object') {
    return false
  }

  for (key in array) {
    if (typeof array[key] === 'object') {
      return this.array_walk_recursive(array[key], funcname, userdata)
    }

    if (typeof userdata !== 'undefined') {
      eval(funcname + '( array [key] , key , userdata  )')
    } else {
      eval(funcname + '(  userdata ) ')
    }
  }

  return true
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
array_walk_recursive ({'a': 'b', 'c': {'d': 'e'}}, 'void', 'userdata');
{% endhighlight %}

Should return

{% highlight javascript %}
array_walk_recursive ({'a': 'b', 'c': {'d': 'e'}}, 'void', 'userdata');{% endhighlight %}

## Example 2

{% highlight javascript %}
array_walk_recursive ('a', 'void', 'userdata');
{% endhighlight %}

Should return

{% highlight javascript %}
array_walk_recursive ('a', 'void', 'userdata');{% endhighlight %}


## Authors


Original by

- Johnny Mast (http://www.phpvrouwen.nl)
