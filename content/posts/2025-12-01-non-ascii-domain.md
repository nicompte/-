+++
title = "Should you have a non-ascii domain name"
date = "2025-12-06"
description = "A practical look at non-ASCII domain names—how IDNs work, why ニコ.com exists, and what trade-offs you should expect in browsers, email, and SEO."
+++

It says so at the top, I'm not Japanese, yet, this website is on [ニコ.com](https://ニコ.com), which is Japanese.

## Does that even work?

Internationalized Domain Names (IDNs) let you use non-ASCII characters in hostnames such as, for example, `ニコ.com` instead of `nico.com`.

Some other people will explain it much better than myself how it works, check [here](https://www.iankduncan.com/engineering/2025-12-01-punycode) for example. But the main point, is that `ニコ.com` transformed into ascii using [Punycode](https://wikipedia.org/wiki/Punycode), and is actually `https://xn--tck4b.com`. Both addresses will resolve to this very website.

## The practical reality

Obviously, `ニコ.com` is the best address possible, because `nico.com` has been bought by some company and isn't available anymore. From an SEO standpoint, it's ideal, ニコ is much less common than Nico, so it will stand out.

The possible drawback, is that you need to be able to type katakanas, `ニ` and `コ`. Should you not be able to do so, it's just a matter of looking at how to say "Nico" in Japanese with your favorite tool of the day. So not really a drawback.

From there, the question of compatibility comes in. To prevent phishing, with for example domains like `gооgle.com`, which is actually `xn--ggle-55da.com` with the `о/o` character confusion, or other weird letter substitutions, some applications will either present `ニコ.com` as `https://xn--tck4b.com`, and some will simply strip the link entirely, so users will have to copy/paste the url manually.

And well, then there are emails. A lot of clients will refuse to accept `something-at-ニコ.com`, so it has to be sent to `something-at-xn--tck4b.com`, which is really not ideal. This might depend on the email provider and their market, of course, but support is inconsistent.

## Should you do it?

If you're comfortable with the tradeoffs, especially around emails, go for it. For personal projects and blogs, the quirks are manageable. For businesses that rely heavily on email communication, that's your business, do whatever you think is best.
