---
layout: page
title: Google Resume
permalink: /google-resume/
noindex: true
---

## Google Projects

### Expression

<h4 class="float-left">iOS Software Engineer (Mountain View, CA)</h4>
<h4 class="float-right">2017 Q2 — Present</h4>
<div class="float-clear"></div>

The Expression team ([go/expression](https://goto.google.com/expression)) seeks to improve the way users communicate.

##### Eng on Eyck iOS Library v1

Eyck ([go/eyck-spec](https://goto.google.com/eyck-spec)) creates a personalized avatar ("Gmoji") and poses from a selfie; it is Google's take on [Bitmoji](https://www.bitmoji.com/) and [Animoji](https://support.apple.com/en-us/HT208190). It was highlighted as #1 in [Google Design's Best of 2017](https://design.google/library/2017-design-google/).

I worked with [Tristan Emrich](https://moma.corp.google.com/person/tristane) and [Arpit Agarwal](https://moma.corp.google.com/person/arpwal) on a new Eyck library which is shipping in Maps and Gboard in 2018 Q1. With the library, Maps users can set an Eyck avatar in place of their blue dot ([go/eyck-maps](https://goto.google.com/eyck-maps), [go/igmm-blue-dot-avatar](https://goto.google.com/igmm-blue-dot-avatar)), and Gboard users can send personalized stickers ([go/gboard-stickers](https://goto.google.com/gboard-stickers)). Some notable accomplishments:

* *Metadata Persistence*. The library's metadata persistence layer handles loading and saving data between launches. I made it more efficient, location-agnostic, stateless, and proto-friendly ([b/73079603](https://b.corp.google.com/issues/73079603)).
* *Binary Size*. Given our clients' sensitivity to binary size changes, I worked to ensure the library binary size was as small as possible (<1MB) ([b/73763651](https://b.corp.google.com/issues/73763651), [b/73898925](https://b.corp.google.com/issues/73898925)).
* *Networking*. The composition of the Eyck iOS networking stack was crucial due to clients' binary size constraints. I worked with [Tristan](https://moma.corp.google.com/person/tristane) to design a networking abstraction to swap dependencies (e.g. gRPC vs GTM) depending on clients' needs ([go/eyck-ios-networking](https://goto.google.com/eyck-ios-networking)).
* *Identity Management*. I guided discussion regarding identity management ([go/eyck-identity-management](https://goto.google.com/eyck-identity-management)).

##### Sole Eng on Improving Code Quality

I had a personal mission to improve code quality. This ensured that code was clean and readable, kept our code building, and improved project pH level [from 1 to 3](https://signals.corp.google.com/#/project/Google%2520%253E%2520Mobile%2520and%2520Digital%2520Content%2520%253E%2520Applications%2520and%2520Services%2520%253E%2520eyck.ios%253Ab%253A3/phlevel_metrics%253A%253Amode-phlevel?view=default&startDate=1517299200&endDate=1519747617.034&period=DAY&subgraphs=eyck.ios%25253Ab%25253A3).

* *Style Guides*.
  * Wrote a brand new style guide for Expression iOS ([b/72119342](https://b.corp.google.com/issues/72119342), [cl/182446332](https://critique.corp.google.com/#review/182446332)).
  * I resolved disagreements between the Google and Fireball iOS [style guide](https://g3doc.corp.google.com/googlemac/iPhone/Fireball/g3doc/developer/styleguide.md) and contributed improvements to the Fireball style guide (e.g. [cl/168558241](https://critique.corp.google.com/#review/168558241), [cl/168558084](https://critique.corp.google.com/#review/168558084)).
* *Automation/Testing*. I added automated checks (e.g. [b/72119324](https://b.corp.google.com/issues/72119324), [go/expression-ios-formatting](https://goto.google.com/expression-ios-formatting)) and testing to ensure code quality remained high.
* *CL Turnaround*. I noticed slow code reviews were impacting our team's output, so I created PLX scripts ([here](https://plx.corp.google.com/script/#a=qo%7Ci=google%3A%3Ascript_5c._1c0a30_12ea_45b1_8d4a_d4733b4cb485), [here](https://plx.corp.google.com/script/#a=qo%7Ci=google%253A%253Ascript_a1._32cffc_7e9d_4ef0_85ca_4f202c60af24)) and a dashboard ([go/clturnaround](https://goto.google.com/clturnaround)) to provide useful metrics such as time to respond to a CL and impact on total review time.

##### TL for Bauhaus iOS

Bauhaus ([go/bauhaus-spec](https://goto.google.com/bauhaus-spec)) is a tool that enables users to edit and collage images before sending them. This was a key expressive differentiator for Fireball (Allo).

* *Web Stickers*. I created a web stickers feature for Bauhaus ([go/ios-bauhaus-web-stickers](https://goto.google.com/ios-bauhaus-web-stickers), [b/63818898](https://b.corp.google.com/issues/63818898)).
  * Contributions spanned all the way from Fireball UI to the Ink library and Boq server modules.
  * Collaborated with Expression, Fireball, and Picasso PMs and designers.
  * Although the volume of web stickers sent is fairly low (~3.5% of stickers sent), users find web stickers to be invaluable for expressions missing in default stickers (~40-50% of all stickers sent after a search are web stickers, more than any other sticker).

##### Eng on Fireball iOS

* *Image Refactor*.
  * While working in Fireball code, I noticed major shortcomings in how images were being handled throughout the Fireball app, resulting in bugs such as png images being converted to jpg and gifs being saved as .jpg.
  * Conducted a large refactor of all image handling code in Fireball, fixing many bugs and making image APIs simpler and more consistent (e.g. [b/64732209](https://b.corp.google.com/issues/64732209), [cl/171324641](https://critique.corp.google.com/#review/171324641)).
  * Added unit tests to new image code, averaging ~80% incremental code coverage during the refactor (up from 0%).
* *UI Polish*. I fixed UI inconsistencies that hurt the user experience ([b/63848954](https://b.corp.google.com/issues/63848954)).

{% include_relative resume_raw.md %}
