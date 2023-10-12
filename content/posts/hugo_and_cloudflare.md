+++
title = "Hugo and Cloudflare"
date = "2023-10-12T18:32:08-04:00"
author = "James Crace"
authorTwitter = "" #do not include @
cover = ""
tags = ["hugo", "cloudflare"]
keywords = ["cloudflare", "hugo"]
description = "Using Hugo with Cloudflare"
showFullContent = false
readingTime = false
hideComments = false
color = "" #color from the theme settings
+++

I recently decided to use Hugo to deploy my personal website. I looked into the various hosting options and opted for Hugo because I like the simplicity of Markdown and static sites, and Hugo seems to be very fast and easy to use. 

I did run into just a couple issue getting it up and running on Cloudflare. You’ll want to create two environment variables in Cloudflare settings, HUGO_VERSION and CF_PAGES_URL. Set the first to the version of Hugo you are using, and set CF_PAGES_URL to https://yourdomain.tld. 

Amend your build command:
```
hugo -b $CF_PAGES_URL
```

Save those changes and rebuild. Internal links should now function properly. 

You can read more about this in the [Cloudflare docs](https://developers.cloudflare.com/pages/framework-guides/deploy-a-hugo-site)

