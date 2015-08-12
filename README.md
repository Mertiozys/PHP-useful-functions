# PHP-useful-functions

A repo with useful PHP functions


## str_replace_between

Even after looking for it for a while, I didn't find anything doing exactly what I needed so I created this function.

This function replaces a string between 2 given strings, with the possibility to keep or remove the given strings.


### Description

string str_replace_between ( string $haystack , mixed $replace , mixed $needleStart , string $needleEnd , bool $keepNeedleStart , bool $keepNeedleEnd, bool $keepAllNeedleStart)

Returns part of **haystack** string with strings between **needleStart** and **needleEnd** replaced by **replace**.


### Arguments

**haystack**
    The input string.

**replace**
    The replacement value that replaces string between **needleStart** and **needleEnd**.

**needleStart**
    The beginning value to search for in **haystack**.

**needleEnd**
    The ending value to search for in **haystack**.

**keepNeedleStart**
    If true, occurrences of **needleStart** will be kept in **haystack**.

**keepNeedleEnd**
    If true, occurrences of **needleEnd** will be kept in **haystack**.

**keepAllNeedleStart**
    If true, occurrences of **needleStart** with no **needleEnd** after will be kept.


### Example

```
$haystack = '1FooIsAwesome_And2FooIsFun3FooIsSmart_And4FooKnowsEverything_AndOver';
$needleStart = 'Foo';
$needleEnd = '_And';
$keepNeedleStart = true;
$keepNeedleEnd = false;
$keepAllNeedleStart = true;

echo str_replace_between($haystack, 'Bar', $needleStart, $needleEnd, $keepNeedleStart, $keepNeedleEnd, $keepAllNeedleStart);

// Will return 1FooBar2FooFooBar4FooBarOver
```
