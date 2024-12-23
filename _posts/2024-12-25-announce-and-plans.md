---
layout: post
title: "Errbit-NG: Announce and plans"
author: biow0lf
date: 2024-12-25 12:00:00 +0100
---

Hi!

Today is 25 Dec 2024 and Christmas. Awesome time to make greet announce.

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

After this, I understand that Errbit developers don't use it in production.

So, what I should do when I need simple and self-hosted error tracker? I fork it.

With all my respect to all original Authors of Errbit and with all my respect to all contributors to original Errbit, We need fresh blood.

Ok, who am I? I am [Igor (Ihor) Zubkov](biow0lf). Software developer from Mariupol, Ukraine. You may see Mariupol in news and see how brave defenders of Ukraine fight with russian occupants.

So, fork goal:

1. Keep errbit instances up-and-running with minimal effort.
2. Keep errbit up-to-date with dependencies (security part).
3. Keep errbit on latest and the best technologies that Rails ecosystem provides. Like: stimulus, turbo, solid_queue.

Before describing any plans, let me show what was already done in fork.

1. [Rails 5.1.7](https://github.com/errbit-ng/errbit-ng/commit/c43b9002e32ea01403e0a1a7f146311e7933d2b8)
2. [Rails 5.2.8.1](https://github.com/errbit-ng/errbit-ng/commit/0c2f5f82481c099916b1230729858a45f4dc918c)
3. [Enable bootsnap](https://github.com/errbit-ng/errbit-ng/commit/f7f0f8a30daa1f4168eee04083460f6e0da348f0)
4. [Ruby to 3.1.6 & Rails to 6.0.6.1](https://github.com/errbit-ng/errbit-ng/commit/1f7b90e7b27edb2dd9f1146086e1dbc1f73f51c2#diff-06572a96a58dc510037d5efa622f9bec8519bc1beab13c9f251e97e657a9d4edR3)
5. [Rails 6.1.7.10](https://github.com/errbit-ng/errbit-ng/commit/830bb976483362d4770af8193b84d0aa54bd19c9)
6. [Enable dependabot](https://github.com/errbit-ng/errbit-ng/commit/3782f44146cb9de40dced16c9ec12bf78493a451)
7. [Bundler: enable CHECKSUMS](https://github.com/errbit-ng/errbit-ng/commit/950e925339ff53e0b12f1660cb92fe5b88bf1619)
8. [Add simplecov gem](https://github.com/errbit-ng/errbit-ng/commit/abd40e8ebb0df6b2e9a19fd8c2599dd8b7266a8a#diff-d09ea66f8227784ff4393d88a19836f321c915ae10031d16c93d67e6283ab55fR85)
9. [Migrate to zeitwerk loader](https://github.com/errbit-ng/errbit-ng/pull/93/commits/48fd0f83ac36e2c51632a86314d3f4783b56cffd)
10. [Improve bundler platforms support (for faster docker image builds)](https://github.com/errbit-ng/errbit-ng/pull/125)
11. [Ruby 3.2.6](https://github.com/errbit-ng/errbit-ng/commit/fc8fa66cd12cc85c1af189da2063984d5c2884cc)
12. [Standardize](standardrb) project
13. [Run test on Ruby 3.1 (for JRuby support), 3.2 and 3.2](https://github.com/errbit-ng/errbit-ng/commit/013e2dfd538ef271f877254bf0d5df854738e8ee#diff-06572a96a58dc510037d5efa622f9bec8519bc1beab13c9f251e97e657a9d4edR4)
14. [JRuby support](https://github.com/errbit-ng/errbit-ng/commit/098b5f339f74085521d09d5ed35064663fe676ca)
15. [Replace poltergeist with selenium-webdriver](https://github.com/errbit-ng/errbit-ng/commit/2f04c1645e42bbf0f0dd8cd1c22a01450659d3a1)
16. [Drop mini_racer gem](https://github.com/errbit-ng/errbit-ng/commit/b1a2aa1dcf7d236b28c15032b0626a89a4d70250#diff-d09ea66f8227784ff4393d88a19836f321c915ae10031d16c93d67e6283ab55fL94)
17. [Ruby 3.3.6](https://github.com/errbit-ng/errbit-ng/commit/6b169f9eabda02f71959aeec627e1e1aadbbe356)

And... Plan:

1. Enable official docker builds
2. Upgrade Ruby on Rails to 7.0.x
3. Upgrade Ruby on Rails to 7.1.x
4. Upgrade Ruby on Rails to 7.2.x
5. Upgrade Ruby on Rails to 8.0.x
6. Remove jQuery
7. Migrate to Turbo and Stimulus

First alpha release in Q1 2025. List of blocking issues:

1. Upgrade Ruby on Rails (at least) to 7.2.x
2. Enable official docker builds
3. Some kind of documentation

First stable release as soon as it will be ready.

[Errbit]: https://github.com/errbit/errbit
[Errbit-NG]: https://github.com/errbit-ng/errbit-ng
[Rails_6.1_upgrade]: https://github.com/errbit/errbit/pull/1533
[biow0lf]: https://github.com/biow0lf
[standardrb]: https://github.com/standardrb/standard
