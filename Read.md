1- first go **Settings** enable *pages*, **Build and deployment** chose deply from *main*
then make changes to

2- _config, in url **Section** change *url*
- _data/setting
- _include/navbar
    /whatsapp
- _sass
- assets
- llms
- robots
- sitemap




Here’s what you need to know:

⸻

1️⃣ Basic rules
    •    Any Markdown or HTML file with front matter (---) becomes a Jekyll page.
    •    You can put it in the root (/read.md) or in a folder.
    •    The permalink front matter determines its URL.

⸻

2️⃣ Example read.md at root
```
---
layout: page
title: "Default SEO Page"
description: "This is a default page to provide fallback Open Graph and SEO data."
image: "/assets/img/default-share.jpg"
permalink: "/read/"
---
```
🔹 What this does
    •    page.title, page.description, page.image → accessible to OG and Twitter tags
    •    page.url → /read/ (from permalink)
    •    Can act as a fallback page if you ever forget to define front matter on another page (though usually better to define per page)

⸻

3️⃣ How to use it as a fallback in _includes/open-graph.html
```
---
layout: page
title: "Website Audit & SEO Services"
description: "Professional website audit and SEO services for businesses in Singapore."
image: "/assets/img/services-share.jpg"
permalink: "/services/"
---
```
•    If a page is missing front matter, Jekyll uses site defaults (_config.yml)
    •    Or you could manually reference /read/ as a fallback:

``` 
<meta property="og:title" content="{{ page.title | default: site.pages | where: 'path', 'read.md' | first.title }}">
```
