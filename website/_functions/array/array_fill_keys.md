---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/array_fill_keys/'
    original by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    bugfixed by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    example:
      - - "keys = {'a': 'foo', 2: 5, 3: 10, 4: 'bar'}"
        - "array_fill_keys(keys, 'banana')"
    returns:
      - - '{"foo": "banana", 5: "banana", 10: "banana", "bar": "banana"}'
function: array_fill_keys
category: array
permalink: /functions/array_fill_keys
redirect_from:
  - /functions/array/array_fill_keys/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function array_fill_keys (keys, value) {
  //  discuss at: http://phpjs.org/functions/array_fill_keys/
  // original by: Brett Zamir (http://brett-zamir.me)
  // bugfixed by: Brett Zamir (http://brett-zamir.me)
  //   example 1: keys = {'a': 'foo', 2: 5, 3: 10, 4: 'bar'}
  //   example 1: array_fill_keys(keys, 'banana')
  //   returns 1: {"foo": "banana", 5: "banana", 10: "banana", "bar": "banana"}

  var retObj = {},
    key = ''

  for (key in keys) {
    retObj[keys[key]] = value
  }

  return retObj
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
keys = {'a': 'foo', 2: 5, 3: 10, 4: 'bar'},array_fill_keys(keys, 'banana')
{% endhighlight %}

Should return

{% highlight javascript %}
keys = {'a': 'foo', 2: 5, 3: 10, 4: 'bar'},array_fill_keys(keys, 'banana'){% endhighlight %}


## Authors


Original by

- Brett Zamir (http://brett-zamir.me)


Bugfixed by

- Brett Zamir (http://brett-zamir.me)
