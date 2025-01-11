# WebService::WTFIsMyIP ![static](https://github.com/uperl/WebService-WTFIsMyIP/workflows/static/badge.svg) ![linux](https://github.com/uperl/WebService-WTFIsMyIP/workflows/linux/badge.svg)

Client for wtfismyip.com

# SYNOPSIS

```perl
use WebService::WTFIsMyIP;

my $wtfismyip = WebService::WTFIsMyIP->new;
say "your IP is", $wtfismyip->json->{IPAddress};
```

# DESCRIPTION

This class provides an interface to the WTF

# CONSTRUCTOR

```perl
my $wtfismyip = WebService::WTFIsMyIP->new(%attributes);
```

Create a new instance of the client.  Attributes available:

- ua

    Should be an instance of [HTTP::AnyUA](https://metacpan.org/pod/HTTP::AnyUA), or any class supported by [HTTP::AnyUA](https://metacpan.org/pod/HTTP::AnyUA).
    [HTTP::Tiny](https://metacpan.org/pod/HTTP::Tiny) is used by default.

- base\_url

    The base URL to use.  `https://wtfismyip.com/` is used by default.

# METHODS

## json

```perl
my %hash = $wtfismyip->json->%*;
```

Returns a hash that contains fields such as `IPAddress` and `ISP`.  The method
is so named after the endpoint that it calls, although the return value is converted
into a Perl hash ref.

# AUTHOR

Graham Ollis <plicease@cpan.org>

# COPYRIGHT AND LICENSE

This software is copyright (c) 2025 by Graham Ollis.

This is free software; you can redistribute it and/or modify it under
the same terms as the Perl 5 programming language system itself.
