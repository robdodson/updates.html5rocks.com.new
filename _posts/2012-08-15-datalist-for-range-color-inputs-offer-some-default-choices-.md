---
layout: post
title: "[datalist] for range/color inputs offer some default choices  "
description: ""
article:
  written_on: 2012-08-15
  updated_on: 2012-08-15
authors:
  - agektmr
tags:
  - forms
  - datalist
permalink: /2012/08/datalist-for-range-color-inputs-offer-some-default-choices
---
Chrome started to support `datalist` for `input[type=text]` in Chrome 20. `datalist` helps developers provide recommended values, while allowing users the liberty to write arbitrary values at the same time. Beginning with Chrome 23, you can use `datalist` for `input[type=range]` and `input[type=color]` as well!

### input[type=range]

`datalist` for `input[type=range]` introduces the ability for developers to show indicators beside the slider as shown below:

![range datalist](http://updates.html5rocks.com/images/AMIfv95wI-tljBVfLjUx45bQD_G870IMz9gFKk62UjQDPebAPTqRmwf6iymwUIrA1wKjvWRqGHWHV80E9eoyWmCrczN1Cdpk6_34FkWJx7Zbu2P7PHJ9TbjMFr5Lqtxpy7X1UmGNYnECOAND1Sz9C4gikKfiqgO22g)

{% highlight HTML %}
<input type="range" value="0" min="0" max="100" list="numbers" />
<datalist id="numbers">
  <option>10</option>
  <option>15</option>
  <option>30</option>
  <option>50</option>
  <option>90</option>
</datalist>
{% endhighlight %}

Moving the slider thumb on the input snaps to each of the ticks so that users can easily adjust to those values.

### input[type=color]

`input[type=color]` is already [supported in Chrome](https://plus.google.com/107085977904914121234/posts/1hb7EsELAPH) and Opera. Users can pick arbitrary color without any help from JavaScript plugins.

By adding `datalist` to `input[type=color]`, users can now pick a color from developer selected color swatches as well as choosing arbitrary color from a color picker by themselves.

![color datalist](http://updates.html5rocks.com/images/AMIfv95jKxjkU1eMa3q85X4ZWRnn7F1CUBPm2TjYxhBGbgZMX3GZ-SQArNUQt3rs3sZbGIh3hI2cYi-MhP8Ja-Zd5A9dms4msySyT8CrjTOGHcvqEe-lpCLJIpbqP4uVD5cvR08tOqECpZK1nm16rOTbGnIHOjxXSA)

{% highlight HTML %}
<input type="color" value="#000000" list="colors" />
<datalist id="colors">
  <option>#ff0000</option>
  <option>#0000ff</option>
  <option>#00ff00</option>
  <option>#ffff00</option>
  <option>#00ffff</option>
</datalist>
{% endhighlight %}

Note that `datalist` for `input[type=color]` only accepts the hex color values (ex. `#ff0000`) and values such as `#f00` or `red` won’t work.

To see these new features in action, visit [a demo page](http://demo.agektmr.com/datalist/).
