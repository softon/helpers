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
      Strings::verifyPattern("XX00xx-***","DEF89gg-7y7");	// hi_There  -->   hi There

      /* 16) Take a short extract from a string */
      Strings::excerpt("What is your name?",13,"...");		// What is your...

      /* 17) Return substring between other strings (or string) */
      Strings::between("<head>Hello World</head>","<head>","</head>");		// Hello World

      /* 18) Concatinate multiple values to a single string */
      Strings::concat("Hello"," World");			// Hello World
      Strings::concat("The"," Hello"," World");		// The Hello World

      /* 19) Escape HTML String */
      Strings::escape("<head>Hello World</head>");		// &lt;head&gt;Hello World&lt;/head&gt;

      /* 20) Assert that passed data can be converted to string */
      Strings::stringable("hi_There");			// no exception is thrown
	  Strings::stringable(["hi there"]);		// InvalidArgumentException

      /* 21) Split a corpus of text into lines. This function splits on "\n", "\r\n", or  mixture of any of them */
      Strings::splitLines("Hello 
      World");									// array("Hello","World")

	  /* 22) Explode a string, filling the remainder with provided defaults */
      Strings::explode("|","Hi|Hello|Ola");		// array("Hi","Hello","Ola")

      /* 23) Retrieve the final part of a string, after the first instance of the needle has been located */
      Strings::offset("The Hello World","The ");		// Hello World

      /* 24) Strip off a specific string from the start of another, if an exact match 
      		 is not found, the original string (haystack) will be returned */
      Strings::ltrim("The Hello World","The ");		// Hello World

      /* 25) Trim non null strings */
      Strings::ntrim("  Hello World  ");		// Hello World

      /* 26) Check a string contains another string */
      Strings::contains("Hello World","World");		// true

      /* 27) Check a string contains one of the provided needles */
      Strings::containsAny("One Two Three Four",array("One","Six"));		// true

      /* 28) Check a string ends with one of the provided needles */
      Strings::endsWithAny("One Two Three Four",array("Four","Six"));		// true

      /* 29) Check a string ends with a specific string */
      Strings::endsWith("One Two Three Four","Four");		// true

      /* 30) Check a string starts with one of the provided needles */
      Strings::startsWithAny("One Two Three Four",array("One","Six"));		// true

      /* 31) Check a string starts with a specific string */
      Strings::startsWith("One Two Three Four","One");		// true

      /* 32) Short cut for json_encode with JSON_PRETTY_PRINT */
      Strings::jsonPretty(array("One","Two"));		
```

<h2>Numbers Class</h2>

Helper functions related to Number manipulations. <br>
<pre><code> use Packaged\Helpers\Numbers;  </code></pre>

```php 
      /* 1) Return if a value is between two values */
      Numbers::between(6,1,3);			// false
      Numbers::between(6,3,8);			// true

      /* 2) Number format integers only, any other string will be returned as is */
      Numbers::format(12345.67,4);		// 12,345.6700

      /* 3) Number format with suffix, for making large numbers human readable */
      Numbers::humanize(10000);			// 10k

      /* 4) Return number's ordinal suffix */
      Numbers::ordinal(23);				// rd
```
