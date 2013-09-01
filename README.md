Labelauty jQuery Plugin
=========

A nice and lightweigth jQuery plugin that gives beauty to checkboxes and 
radio buttons and allows custom labels for each status of (un)checked inputs.

Demo: http://francisconeves.com/labelauty/


Installation
------------

Include jQuery, [jquery-labelauty.js], [jquery-labelauty.css] and [images] folder in your project.


Fast Usage
-----------

Write your checkbox or radio input in `body` section and call `labelauty()` to beautify it.
Note: Call plugin when document is ready. See below:

~~~ html
<input type="checkbox"/>
~~~

~~~ js
$(document).ready(function(){
	$(":checkbox").labelauty();
});
~~~

Simple, isn't it?


Use Cases
----------

 * If you want to create user-friendly websites, this is the right choice!

 * Very useful in `remember me` checkboxes, in `settings panel`, etc.


How does it work ?
--------------

The above case will generate one checkbox with default 
labels "Checked" and "Unchecked", one for each input status.

You can change the default labels (see [Options] section) or 
give custom labels to each checkbox, like the following example:

~~~ html
<input type="checkbox" data-labelauty="Don't synchronize files|Synchronize my files"/>
~~~

~~~ js
$(document).ready(function(){
	$(":checkbox").labelauty();
});
~~~

The __data-labelauty__ attribute of radio and checkbox inputs let you write custom label for the __unchecked|checked__ case.
Pipe character __|__, is the default separator between these two labels. You can change this (see [Options] section).




The __data-labelauty__ attribute can be used in three different ways:
__________
__Unchecked|Checked__

To choose a custom label for Unchecked and Checked status.

~~~ html
<input type="checkbox" data-labelauty="Don't synchronize files|Synchronize my files"/>
~~~
__________
__Message__

Without separator, the __Message__ text will be the permament label. It means that label will not change between input status.

~~~ html
<input type="checkbox" data-labelauty="Synchronize my files"/>
~~~
__________
__Omited__

By omiting this attribute, the default labels will be shown.

~~~ html
<input type="checkbox"/>
~~~


Options
-------------

Set a new `class` value that will be applied to changed inputs.

~~~ js
$(":checkbox").labelauty({ class: "myclass" });
~~~

When `label` is setted to `false`, only the input icon appears and changes.

~~~ js
$(":checkbox").labelauty({ label: false });
~~~

Change separator between custom labels, in __data-labelauty__ attribute.
Choose your separator with `separator`.

~~~ js
$(":checkbox").labelauty({ separator: "-" });
~~~

Do you want another default labels?
Set new text in `checked_label` and `unchecked_label`.

~~~ js
$(":checkbox").labelauty({
	checked_label: "You selected this",
	unchecked_label: "You don't want it"
});
~~~

Actually, custom labels has different number of characters or width.
So, you can set `minimum-width` to custom CSS option.

~~~ js
$(":checkbox").labelauty({ minimum_width: "170px" });
~~~

If you dislike the previous option, then you can set labels with same width.
Just set `same_width` to `true`.

~~~ js
$(":checkbox").labelauty({ same_width: true });
~~~


Customization
-------------

You are free to customize all styles included in Labelauty jQuery Plugin.

Just edit [jquery-labelauty.css] to your liking and change images as you wish.


The included CSS file is tiny and simple. Don't be afraid to change it.


Acknowledgements
----------------

© 2013, Francisco Neves. Released under the [MIT License](License.md).

**Labelauty** is authored and maintained by [Francisco Neves][francisconeves].
[Contributors][c] can help to make this plugin better.

 * [My website](http://francisconeves.com) (francisconeves.com)
 * [Github](http://github.com/francisconeves) (@francisconeves)
 * [Twitter](http://twitter.com/fntneves) (@fntneves)

[francisconeves]: http://www.francisconeves.com
[c]:   http://github.com/francisconeves/labelauty-jquery/contributors
[jquery-labelauty.js]: https://github.com/francisconeves/labelauty-jquery/blob/master/source/jquery-labelauty.js
[jquery-labelauty.css]: https://github.com/francisconeves/labelauty-jquery/blob/master/source/jquery-labelauty.css
[images]: https://github.com/francisconeves/labelauty-jquery/tree/master/source/images
[Options]: https://github.com/francisconeves/labelauty-jquery#options

