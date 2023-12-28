<p align="center">
<a href="https://github.com/valorin/random/actions"><img src="https://github.com/valorin/random/workflows/tests/badge.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/valorin/random"><img src="https://img.shields.io/packagist/dt/valorin/random" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/valorin/random"><img src="https://img.shields.io/packagist/v/valorin/random" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/valorin/random"><img src="https://img.shields.io/packagist/l/valorin/random" alt="License"></a>
</p>

# Random by Valorin

Random is a simple helper package designed to make it easy to generate a range of different cryptographically secure random values in PHP apps.

Random was created because I was constantly encountering weak and insecure random value generations within apps during 
my [Laravel and PHP Security Audits](https://valorinsecurity.com/) and I wanted a secure solution to point my clients to
without needing them to implement secure algorithms themselves. The idea was then expanded out a bit to support all of 
the common random value types I've encountered.

## Installation

You can install the package via composer:

```bash
composer require valorin/random
```

There is no need to install any service providers, Random should just work out of the box.

Random is supported on PHP 8.3 and later.

## Usage

Random is designed to be as simple as possible to use. It's a static class, so you can just call the methods directly.

Import the class into your namespace:

```php
use Valorin\Random\Random;
```

### Random numbers

Generate a random number between `$min`, and `$max` (inclusive):

```php
return Random::number(int $min, int $max): int;
```



### TODO

```php

Random::nonce($length, $prefix = '0', $alpha = false): string => prefixed with 0's
Random::string($length, $lower, $upper, $numbers, $symbols, $withEverything): string
Random::letters($length, $withEverything) -> alpha string
Random::alphanum($length, $withEverything) -> alphanum string
Random::password($length, $withEverything) -> everything
Random::passwordWithEverything($length) -> everything
Random::shuffle(array|collection)
Random::select($count)
Random::use(randomizer);
Random::with(randomizer)->number()
Random::token()
```

## Contributing

Contributions are very welcome! There isn't a formal guide, but throw in an Issue or PR and we'll go from there.

## Security Vulnerabilities

Please report any security vulnerabilities via the [GitHub project](https://github.com/valorin/random) 
or by contacting [Stephen Rees-Carter directly](https://stephenreescarter.net/.well-known/security.txt). 

## License

Random is open-source software licensed under the [MIT license](LICENSE.md).
