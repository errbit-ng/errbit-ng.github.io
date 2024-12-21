---
layout: post
title: "Errbit-NG: Announce and plans"
author: biow0lf
date: 2023-12-25 12:00:00 +0100
---

Hi!

Today is Christmas and awesome time to make greet announce.

I am announcing fork of [Errbit](Errbit). Welcome, [Errbit-NG](Errbit-NG)!

So, why to fork, you will ask me?

Current development of Errbit is stale. I try hard to make a bunch of changes to keep it up-to-date and working. Anyone can see my PRs to Errbit:

1. [errbit#1520](https://github.com/errbit/errbit/pull/1520) -- My first PR updates Ruby from 2.7.5 to 2.7.6, puma and nokogiri. All this updates contain CVE fixes (security).
2. [errbit#1522](https://github.com/errbit/errbit/pull/1522) -- Remove unless binstubs and fix bin/rails and bin/rake binstubs.
3. [errbit#1523](https://github.com/errbit/errbit/pull/1523) -- Update `mini_racer` gem (so, errbit can be run-ed on modern macOS).
4. [errbit#1525](https://github.com/errbit/errbit/pull/1525) -- Remove `Rack::Deflater` (just use http cache server or reverse proxy like `nginx` or `traefik`).
5. [errbit#1526](https://github.com/errbit/errbit/pull/1526) -- Just another bunch of dependencies updates.
6. [errbit#1528](https://github.com/errbit/errbit/pull/1528) -- Remove GEMFILE_RUBY_VERSION.
7. [errbit#1530](https://github.com/errbit/errbit/pull/1530) -- Rails 5.0 upgrade.
8. [errbit#1531](https://github.com/errbit/errbit/pull/1531) -- Migrate to GitHub Actions, update gems, improve security with `omniauth-rails_csrf_protection` gem.

And then, PR with [Rails 6.1 upgrade](Rails_6.1_upgrade) stuck from Aug 27, 2022.

[Errbit]: https://github.com/errbit/errbit
[Errbit-NG]: https://github.com/errbit-ng/errbit-ng
[Rails_6.1_upgrade]: https://github.com/errbit/errbit/pull/1533
