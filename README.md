Labelauty jQuery Plugin
=========

A nice and lightweigth jQuery plugin that gives beauty to checkboxes and 
radio buttons and allows custom labels for each status of (un)checked inputs.


Installation
------------

Include jQuery, [labelauty-jquery.js], [labelauty-jquery.css] and [images] folder to your project.


Fast Usage
-----------

Write your checkbox or radio input in `body` section and call `labelauty()` to beautify it.
Note: Call plugin when document is ready. See below:

~~~ html
<input type="checkbox" class="to-labelauty" />
~~~

~~~ js
$(document).ready(function(){
	$(".to-labelauty").labelauty();
});
~~~

Simple, isn't it?


Use Cases
----------

 * Easy to user read what choice he's going to make, when submission occurs.

 * Very useful in Remember Me checkboxes, in website Settins Panel, etc.


How does it work ?
--------------

The above case will generate one checkbox with default 
labels "Checked" and "Unchecked", one for each input status.

You can change the default labels (see [Options] section) or 
give custom labels to each checkbox, like the following example:

~~~ html
<input class="to-labelauty" type="checkbox" data-labelauty="Don't synchronize files|Synchronize my files"/>
~~~

~~~ js
$(document).ready(function(){
	$(".to-labelauty").labelauty();
});
~~~

The __data-labelauty__ attribute of radio and checkbox inputs let you write custom label for the __unchecked|checked__ case.
Pipe character __|__, is the default separator between these two labels. You can change this (see [Options] section).




The __data-labelauty__ attribute can be used in three different ways:
__________
__Unchecked|Checked__

To choose a custom label for Unchecked and Checked status.

~~~ html
<input class="to-labelauty" type="checkbox" data-labelauty="Don't synchronize files|Synchronize my files"/>
~~~
__________
__Message__

Without separator, the __Message__ text will be the permament label. It means that label will not change between input status.

~~~ js
<input class="to-labelauty" type="checkbox" data-labelauty="Synchronize my files"/>
~~~
__________
__Ommited__

By ommiting this attribute, the default labels will be shown.

~~~ html
<input class="to-labelauty" type="checkbox"/>
~~~


Options
-------------

Set a new `class` value that will be applied to changed inputs.

~~~ js
$(".to-labelauty").labelauty({ class: "myclass" });
~~~

When `label` is setted to `false`, only the input icon appears and changes.

~~~ js
$(".to-labelauty").labelauty({ label: false });
~~~

Change separator between custom labels, in __data-labelauty__ attribute.
Choose your separator with `separator`.

~~~ js
$(".to-labelauty").labelauty({ separator: "-" });
~~~

Do you want another default labels?
Set new text in `checked_label` and `unchecked_label`.

~~~ js
$(".to-labelauty").labelauty({
	checked_label: "You selected this",
	unchecked_label: "You don't want it"
});
~~~

Actually, custom labels has different number of characters or width.
So, you can set `minimum-width` to custom CSS option.

~~~ js
$(".to-labelauty").labelauty({ minimum_width: "170px" });
~~~

If you dislike the previous option, then you can set labels with same width.
Just set `same_width` to `true`.

~~~ js
$(".to-labelauty").labelauty({ same_width: true });
~~~


Customization
-------------

You are free to customize all styles included in Labelauty jQuery Plugin.

Just edit `jquery-labeulauty.css` to your liking and change images as you wish.


The included CSS file is tiny and simple. Don't be afraid to change it.


Acknowledgements
----------------

© 2013, Francisco Neves. Released under the [MIT License](License.md).

**Labelauty** is authored and maintained by [Francisco Neves][francisconeves].
[Contributors][c] can help to improve this plugin.

 * [My website](http://francisconeves.com) (francisconeves.com)
 * [Github](http://github.com/francisconeves) (@francisconeves)
 * [Twitter](http://twitter.com/fntneves) (@fntneves)

[francisconeves]: http://www.francisconeves.com
[c]:   http://github.com/francisconeves/labelauty-jquery/contributors
[labelauty-jquery.js]: http://r
[labelauty-jquery.css]: http://r
[Options]: https://github.com/francisconeves/labelauty-jquery#options

