---
layout: post
title: Articles summary - what every programmer should know about.
---

## CPU and memory

[Ulrich Drepper - What Every Programmer Should Know About Memory](http://www.akkadia.org/drepper/cpumemory.pdf)

Take away:

Memory architecture is very complex: caches of different size on speed, several cores which could share data. Locality of memory access in time and space lead to serious benefit in execution time.

## What Every Programmer Should Know About SEO.

[kate{mats} - What Every Programmer Should Know About SEO](http://katemats.com/what-every-programmer-should-know-about-seo/)

Take away:

1. Use alt for pictures, use actual keywords, emphasize titles with H-tags;
2. Use standard urls, make sure content is crawable;
3. Don't put too many links on page to not be classified as spam;
4. Update content often. Websearch will notice that your site is changing and will apply shorter periods to recrawl;

## 10 Things Every Java Programmer Should Know about String.

[10 Things Every Java Programmer Should Know about String](http://javarevisited.blogspot.sg/2013/07/java-string-tutorial-and-examples-beginners-programming.html)

Take away:

1. String backed by char[], they are immutable and final;
2. JVM caches them in String pool -> don't keep sensitive data in strings;
3. String can have different encoding. If you don't know encoding, you can't interpret String correctly;
4. SubString creates new instance in last versions of java (to avoid memory leaks). This could make additional pressure on gc;
5. Split uses regexes, therefore it is slow.

## What should every programmer know about security.

[stackoverflow - What should every programmer know about security?](http://stackoverflow.com/questions/2794016/what-should-every-programmer-know-about-security)

Take away:

1. Don't trust any input, use whitelists instead of blacklists;
2. Decrease complexity;
3. Adhere principle of last privilege;
4. Use well-tested frameworks/libraries instead of own code.

## What every web developer must know about URL encoding.

[Stéphane Épardaud - What every web developer must know about URL encoding](http://blog.lunatech.com/2009/02/03/what-every-web-developer-must-know-about-url-encoding)

Take away:

1. Reserved characters are different for each segment of URL;
2. Use pynny-code encoding for hostnames and percent-encoding for the rest;
3. analyze url before decoding, since after reserved characters appears and segment borders may change;
4. Original -> Decode -> Encode -> Reencoded. Reencoded may differ from Original with same reason. Decoded URL may be valid without encoding;
5. Java URLEncoder/URLDecoder can't be used for whole URL: they are for HTML form encoding. Best suits query part;
6. Construct URL from properly encoded parts;
7. If you need path segments - be sure you do use unencoded path;


## Every Computer Scientist Should Know About Floating-Point Arithmetic.

[Goldberg - What Every Computer Scientist Should Know About Floating-Point Arithmetic](http://docs.oracle.com/cd/E19957-01/806-3568/ncg_goldberg.html)

Take away:

1. Floating-point number consist from **base** and **precision**.
0.1 (base=10, pr=3) = 1.00 * 10^(-1);
0.1 (base=2, pr=24) =[approx]> 1.10011001100110011001101 * 2^(-4);
2. Floating-point repr. could be not unique;
3. IEEE 754 assume **base**=2, **pr**=24 (single precision) and **pr**=53 (double precision);
4. IEEE 854 assume **base**=(2 OR 10), **pr**=24 (single precision) and **pr**=53 (double precision);
5. In IEEE std. zero could have sign;
## What every programmer needs to know about game networking.

## What technical details should a programmer of a web application consider before making the site public.

## Time.

## The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets.
