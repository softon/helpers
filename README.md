Generic Helper Library
=======

[![Latest Stable Version](https://poser.pugx.org/packaged/helpers/version.png)](https://packagist.org/packages/packaged/helpers)
[![Total Downloads](https://poser.pugx.org/packaged/helpers/d/total.png)](https://packagist.org/packages/packaged/helpers)
[![Build Status](https://travis-ci.org/packaged/helpers.png)](https://travis-ci.org/packaged/helpers)
[![Dependency Status](https://www.versioneye.com/php/packaged:helpers/badge.png)](https://www.versioneye.com/php/packaged:helpers)
[![HHVM Status](http://hhvm.h4cc.de/badge/packaged/helpers.png)](http://hhvm.h4cc.de/package/packaged/helpers)
[![Coverage Status](https://coveralls.io/repos/packaged/helpers/badge.png)](https://coveralls.io/r/packaged/helpers)

Some useful functions & helper classes

<h2>Strings Class</h2>

Helper functions related to string manipulations. <br>
<pre><code> use Packaged\Helpers\Strings;  </code></pre>

```php 
      /* 1) Split a camel case string to words */
      Strings::splitOnCamelCase("hiThere");			// hiThere  -->   hi There

      /* 2) Split a string on underscores */
      Strings::splitOnUnderscores("hi_There");			// hi_There  -->   hi There

      /* 3) Convert a string to an underscored string */
      Strings::stringToUnderScore("hiThere");			// hiThere  -->   hi_there

      /* 4) Convert a string to camel case */
      Strings::stringToCamelCase("hi_there");			// hi_There  -->   hiThere

      /* 5) Convert a string to pascal case */
      Strings::stringToPascalCase("hi_there");			// hi_there  -->   Hi There

      /* 6) Convert a string to human readable, capitalising every word */
      Strings::titleize("hiThere",true);				// hiThere  -->   Hi There
      Strings::titleize("hi_there",false);				// hi_there  -->   Hi There

      /* 7) Convert a string to a human readable one */
      Strings::humanize("hiThere",true);				// hiThere  -->   Hi there
      Strings::humanize("hi_there",false);				// hi_there  -->   Hi there

      /* 8) Hyphenate a string, converting spaces and underscores to hyphens */
      Strings::hyphenate("hi_There");					// hi_There  -->   hi-There

      /* 9) Convert a string to a nice url friendly format */
      Strings::urlize("hi_There");						// hi_There  -->   hi-there

      /* 10) Split a string into an array based on expected human input */
      Strings::stringToRange("1-3");					// array(1,2,3)
      Strings::stringToRange("1,4,6,7");				// array(1,4,6,7)

      /* 11) Find the common start between two strings */
      Strings::commonPrefix("abc","abcdef");			// abc

      /* 12) Split a string at a specific character position */
      Strings::splitAt("abcde",3);						// array("abc","de")

      /* 13) Generate a random string of $length bytes */
      Strings::randomString(6);							// C9Ej6S

      /* 14) Generate random string based on pattern */
      Strings::pattern("XX000XX-0X");					// HK847GW-6F

      /* 15) Verify string to comply to a pattern  */
      Strings::verifyPattern("XX00xx-***","DEF89gg-7y7");			// hi_There  -->   hi There

      /* 11) Find the common start between two strings */
      Strings::commonPrefix("hi_There");			// hi_There  -->   hi There

      /* 11) Find the common start between two strings */
      Strings::commonPrefix("hi_There");			// hi_There  -->   hi There

      /* 11) Find the common start between two strings */
      Strings::commonPrefix("hi_There");			// hi_There  -->   hi There

      /* 11) Find the common start between two strings */
      Strings::commonPrefix("hi_There");			// hi_There  -->   hi There

      /* 11) Find the common start between two strings */
      Strings::commonPrefix("hi_There");			// hi_There  -->   hi There

      /* 11) Find the common start between two strings */
      Strings::commonPrefix("hi_There");			// hi_There  -->   hi There





```
