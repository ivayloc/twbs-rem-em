Bootstrap rewritten with em and rem units
===========

This is Bootstrap v3.2.0 and has been rewritten to support rem and em units. I have use David Ensinger's mixin for px to rem conversion and for px to em conversion is used Tobias Sjösten's @mixin.

There is no need to do any calculation to have responsive mobilefirst webside written with em and rem units, you can accomplish this with the two build in @mixins rem(property, values) and em(values).

Example:

h1 { 
  @include rem(magrin, 3px 0 5px 10px);
  padding: em(5px) em(3px)
}

Yields:

h1 {
  margin: 3px 0 5px 10px;
  margin: 0.188em 0 0.313em 0.625em;
  padding: 0.313em 0.188em;
}

