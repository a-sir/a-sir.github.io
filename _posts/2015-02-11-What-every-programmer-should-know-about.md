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

[What every programmer needs to know about game networking](http://gafferongames.com/networking-for-game-programmers/what-every-programmer-needs-to-know-about-game-networking/)

Take away:

1. First approach was peer-to-peer connections, when local machine receives commands of all players; Bad things: not synchronized movements on all machines, only for LAN;
2. Secondly client-server scheme was used, it was better in latency but still not responcive enough;
3. Then Carmack in Quake allowed local machine to predict movements of other player till it receives real actions.


## What technical details should a programmer of a web application consider before making the site public.

[stackexchange - What technical details should a programmer of a web application consider before making the site public](http://programmers.stackexchange.com/questions/46716/what-technical-details-should-a-programmer-of-a-web-application-consider-before)

Take away:

1. Test across different browsers and mobile;
2. Plan how to deploy updates, setup good logging, automate backups;
3. Redirect after POST to prevent refresh cycle;
4. Use caching, optimal image size, gzip/deflate;

## Time.

[unix4lyfe.org - Time](https://unix4lyfe.org/time/)

Take away:

1. UTC=GMT = Greenwich time. Other timezones have offset from UTC;
2. epoch its seconds from UTC beginning of 1970;
3. Timezones is a presentation problem. Better to use UTC in software.

## The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets.

[Joel Spolsky - The Absolute Minimum Every Software Developer Absolutely, Positively Must Know About Unicode and Character Sets](http://www.joelonsoftware.com/articles/Unicode.html)

1. Unicode is a set of code points. Each letter has own code point, but Unicode don't say anything about physical way to keep letter in memory;
2. Encoding determine that. First encodings used 2 bytes for each code point, but they may keep bytes in direct or reverted order to make processing faster;
3. Most of letters in English use 1 byte, therefore UTF-8 was invented to save space. 1 byte for code points 0-127 and up to 6 bytes for upper code points.
