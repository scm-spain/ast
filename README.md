# AppNexus Seller Tag
The AppNexus Seller Tag (AST) is a lightweight JavaScript SDK that runs in the header or body of a web page in a user's browser and allows publishers to conduct auctions directly from the page. AST consolidates all ad slots on a page to be auctioned and sends information about them in a single ad request whenever possible. AST loads asynchronously, meaning that ad calls do not block the page content from loading.

## Introduction

Schibsted spain is not the owner of this library, this is only a wrapper to be able to push it to npm package manager until AppNexus decide to do it by their self.

## How to use it

import it with require 

```
require('@schibstedspain/ast')
```

## AST Release History

### 0.8.0
### Breaking Change
This version of AST contains breaking changes. It will not be promoted to the production version of AST until on or after July 10, 2017. For more details about out breaking change policy, please refer to the Breaking Changes - AST API wiki page.
* Support v3native assets. Changes consist of:
  * The adTypeobjectreturnedfornativedemandwillbechanging to support our new native asset model, and to be more aligned with the OpenRTB native standard.
  * The following fields have been renamed:
      * description renamed to body
      * mainMedia renamed to image
  * The following fields have been removed:
      * custom
      * rating
  * The following fields have been moved:
      * iconImgUrl has been moved under the icon object to icon.url
* Improvement in page performance by reducing the number of times our Viewability javascript can be inserted to once per page (instead of once per ad slot)
* Minor bug fixes