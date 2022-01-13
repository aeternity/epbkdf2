epbkdf2
=====

Simplistic library implementing
[PBKDF2](https://datatracker.ietf.org/doc/html/rfc6070) in Erlang.

Note: Similar functionality was added in
[OTP-24.2](https://www.erlang.org/news/152) so it is expected that this library
becomes obsolete in a couple of years time (yeah, right...).


Usage
-----

For example to use PBKDF2 with SHA512-HMAC (2048 iterations):
```
3> epbkdf2:pbkdf2(sha512, <<"Passwd">>, <<"Some salt">>, 2048).
{ok,<<231,76,71,218,90,40,181,108,252,147,38,142,162,15,
      11,101,1,202,64,243,130,144,163,58,195,0,254,...>>}
```


Build
-----

    $ rebar3 compile
