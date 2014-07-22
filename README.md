Bootstrap rewritten with em and rem units
===========

This is Bootstrap v3.2.0 and has been rewritten to support rem and em units. I have use [David Ensinger][DavidEnsinger]'s mixin for px to rem conversion and for px to em conversion is used [Tobias Sjösten][TobiasSjösten]'s function.

There is no need to do any calculation to have responsive mobilefirst webside written with em and rem units, you can accomplish this with a @mixins `rem(property, values)` and with this function `em(values)`.

<b>Example:</b>

<pre class="console">
h1 { 
  @include rem(margin, 3px 0 5px 10px);
  padding: em(5px) em(3px)
}
</pre>

<b>Yields:</b>

<pre class="console">
h1 {
  margin: 3px 0 5px 10px;
  margin: 0.1875rem 0 0.3125rem 0.625rem;
  padding: 0.313em 0.188em;
}
</pre>


[DavidEnsinger]: http://davidensinger.com/2013/03/using-rems-with-sass/
[TobiasSjösten]: http://vvv.tobiassjosten.net/css/px-to-em-with-sass/
