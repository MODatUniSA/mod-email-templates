# MOD. email newsletters

This repository contains the responsive email newsletter designs for [MOD](http://mod.org.au).

We've designed our email newsletters using [MJML](https://mjml.io) so that we can focus on how they look rather than making them work on *all* of the email clients.

<img src="https://raw.githubusercontent.com/MODatUniSA/mod-email-templates/master/mod-newsletter.jpg" width="100%" />

## Generation

To generate the HTML from the `.mjml` templates, install the [MJML command line tools](https://mjml.io/download), and then run:

`$ mjml mod-newsletter.mjml`

That should output a corresponding HTML file: `mod-newsletter.html`

## Post processing

There are a few little hacks that are needed to get the Campaign Monitor tags working nicely. Here is the post-processing work needed.

1. Fix the empty `<repeater></repeater>` tags that are generated next to each other rather than an open tag at the start and a close tag at the end.
2. Add `editable` to the hero `<img />` tag so that our team can edit the top image if need be.
