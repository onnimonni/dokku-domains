[![Build Status](https://travis-ci.org/krisrang/dokku-domains.png?branch=master)](https://travis-ci.org/krisrang/dokku-domains)

Dokku domains plugin
=====

This fork is just listening both http and https protocols and not doing redirects if ssl is in use.
It also uses automatically ssl keys from dokku root if they are placed in /ssl folder

Installation
-----

* Requires Ruby >= 1.9.3 present on the host

```bash
git clone https://github.com/onnimonni/dokku-domains.git /var/lib/dokku/plugins/domains
```

Commands
-----

```bash
$ dokku help
    domains <app>                                   display the domains for an app
    domains:set <app> DOMAIN1 [DOMAIN2 ...]         set one or more domains
```

Sample usage
-----

Add extra domains for superapp:

```bash
$ dokku domains:set superapp www.superapp.com ssl.superapp.com
-----> Setting superapp domains to: www.superapp.com ssl.superapp.com
```

Now superapp will respond to superapp.HOST, www.superapp.com and ssl.superapp.com

TODO
-----
* Add tests
* Add domains:add and domains:remove commands

License
-----
MIT
