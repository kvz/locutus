---
params:
  headKeys:
    discuss at:
      - - 'http://phpjs.org/functions/array_values/'
    original by:
      - - 'Kevin van Zonneveld (http://kevin.vanzonneveld.net)'
    improved by:
      - - 'Brett Zamir (http://brett-zamir.me)'
    example:
      - - "array_values( {firstname: 'Kevin', surname: 'van Zonneveld'} );"
    returns:
      - - "{0: 'Kevin', 1: 'van Zonneveld'}"
function: array_values
category: array
permalink: /functions/array_values
redirect_from:
  - /functions/array/array_values/
---

<!-- WARNING! This file is auto generated by `npm run web:inject`, do not edit by hand -->

Here's what a JavaScript equivalent for PHP’s array_chunk might look like

{% highlight javascript %}
function array_values (input) {
  //  discuss at: http://phpjs.org/functions/array_values/
  // original by: Kevin van Zonneveld (http://kevin.vanzonneveld.net)
  // improved by: Brett Zamir (http://brett-zamir.me)
  //   example 1: array_values( {firstname: 'Kevin', surname: 'van Zonneveld'} );
  //   returns 1: {0: 'Kevin', 1: 'van Zonneveld'}

  var tmp_arr = [],
    key = ''

  if (input && typeof input === 'object' && input.change_key_case) {
    // Duck-type check for our own array()-created PHPJS_Array
    return input.values()
  }

  for (key in input) {
    tmp_arr[tmp_arr.length] = input[key]
  }

  return tmp_arr
}

{% endhighlight %}

## Example 1

{% highlight javascript %}
array_values( {firstname: 'Kevin', surname: 'van Zonneveld'} );
{% endhighlight %}

Should return

{% highlight javascript %}
array_values( {firstname: 'Kevin', surname: 'van Zonneveld'} );{% endhighlight %}


## Authors


Original by

- Kevin van Zonneveld (http://kevin.vanzonneveld.net)


Improved by

- Brett Zamir (http://brett-zamir.me)
