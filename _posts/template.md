---
title: TITLE
description: Short summary of the post.
date: YYYY-MM-DD HH:MM:SS +/-TTTT
categories: [TOP_CATEGORIE, SUB_CATEGORIE] # max 2 categories
tags: [TAG]     # TAG names should always be lowercase
toc: false
comments: false
pin: false
media_subpath: /path/to/media/directory
image:
  path: /path/to/image
  alt: image alternative text
---

Si le media_subpath est defini on peut directement mettre le nom de fichier, pas besoin du chemin.
![img-description](img.extension) _Image Caption_

To prevent the page content layout from shifting when the image is loaded, we should set the width and height for each image.
![Desktop View](/assets/img/sample/mockup.png){: w="700" h="400" }

![Desktop View](/assets/img/sample/mockup.png){: .normal }
![Desktop View](/assets/img/sample/mockup.png){: .left }
![Desktop View](/assets/img/sample/mockup.png){: .right }
![Desktop View](/assets/img/sample/mockup.png){: .shadow }

specify size: w="xxx" h="xxx"
left aligned: .w-75 .normal
flot left: .w-50 .left
flot right: .w-50 .right

direction, size and shadow can be mixed
![Desktop View](/path/to/image){: w="700" h="400".left .shadow }

---

footnote in text are made with[^footnote1] and maybe[^footnote2]

en base de la page mettre: 
## Les references:
[^footnote1]: la premiere
[^footnote2]: la deuxieme
---

Video include:
{% include embed/youtube.html id='' %}

apple podcast inclusion
{% include embed/applepodcast.html id='' %}

apple podcast episode inclusions
{% include embed/applepodcastep.html id='' %}

---

> Ceci est un message d'information.
{: .prompt-info }

> Ceci est une idée.
{: .prompt-tip }

> Ceci est un avertissement
{: .prompt-warning }

> Ceci est un danger
{: .prompt-danger }