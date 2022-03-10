---
date: "2018-09-01T00:00:00Z"
draft: true
title: Mechanics behind this blog
---

I thought it would be interesting to describe how this blog works. Perhaps that would be useful, or others can learn and improve upon it.

#### Domain stuff
I register this blog through Google Domains. Yes, I know there are cheaper ways, but I buy a few things from them anyway. They also obscure the ownership of the domain, which typically is a premium/upsell on many cheap domain registrars and can end up being more expensive. 

On Google, it's configured to send requests for this domain over to CloudFront, which is operating as the CDN.

#### Jekyll
This is a static site framework, typically affiliated with GitHub Pages. I actually ran the blog for awhile completely off of GitHub pages; however, I wanted to move to HTTPS and found (at the time, anyway), that doing so on GH Pages was going to be complicated. Doable for sure, but I'd have to handle the certificate and redirects somewhere else. I found it to be easier to move the static website to S3 rather than coordinating everything to keep GHPages in the mix.

#### HTTPS / Certificate
I use the AWS Certificate Manager here. I won't claim to be a wizard with redirects, but I need to be sure that traffic gets redirected/routed through the HTTPS cert, and I feel I've accomplished that.

#### S3 Website uploads



#### CloudFront as a CDN


#### Log analysis