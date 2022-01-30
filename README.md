<svg width="80" viewBox="0 0 1446 746" xmlns="http://www.w3.org/2000/svg" class="c">
<path d="M393.799 328.184L66.0496 656.349L0.50885 590.726L262.718 328.184L0.50885 65.6417L66.0496 0.064209L393.799 328.184Z" fill="#dedede"/>
<path d="M1424.04 74.5625C1424.04 115.95 1390.93 149.061 1350.37 149.061C1309.81 149.061 1276.7 115.95 1275.87 74.5625C1275.87 33.1746 1309.81 0.064209 1350.37 0.064209C1390.93 0.064209 1424.04 34.0016 1424.04 74.5625ZM1398.38 325.374C1410.8 324.547 1423.21 329.513 1432.32 338.617L1432.32 338.621C1441.42 347.726 1446.39 360.142 1444.73 373.386L1424.87 602.675C1423.21 625.853 1404.18 643.236 1381 643.236H1377.69C1353.68 640.751 1335.47 619.23 1337.13 595.224L1352.03 417.256L1292.43 420.568C1307.33 450.367 1315.61 484.304 1315.61 519.899C1315.61 579.497 1292.43 634.129 1254.35 674.69L1197.24 617.573C1221.24 591.913 1235.31 557.147 1235.31 519.898C1235.31 439.606 1169.92 374.213 1089.63 374.213C1052.38 374.213 1017.61 389.11 991.953 412.289L934.836 355.173C967.119 324.547 1007.68 303.853 1053.21 296.403L1163.3 169.755L1101.22 133.333L1025.89 200.381C1007.68 216.936 980.363 215.279 963.808 197.07C947.253 178.86 948.91 151.543 967.12 134.988L1066.45 46.4175C1080.52 34.001 1101.22 31.5197 1117.77 41.4515L1320.57 159.821C1331.33 166.444 1337.95 176.376 1340.44 187.965C1345.4 204.521 1342.09 222.733 1329.68 236.804L1244.42 333.652L1398.38 325.374ZM1078.46 664.33C1003.36 658.603 943.94 595.604 943.94 519.069C943.94 488.443 953.044 461.126 968.772 437.121L910.829 379.178C881.031 417.254 862.818 466.092 862.818 518.241C863.184 574.077 883.017 624.925 915.792 664.33H393.799V745.875H1080.97V745.713C1083.84 745.82 1086.73 745.875 1089.62 745.875C1142.6 745.875 1190.61 727.665 1228.69 697.863L1170.74 639.92C1147.57 655.648 1120.25 664.753 1089.62 664.753L1089.63 664.754C1086.72 664.754 1083.83 664.669 1080.97 664.5V664.33H1078.46Z" fill="#dedede" />
</svg>

# a11y.build
This is the source for [a11y.build](https://a11y.build), a site dedicated to teaching HTML, CSS, and JavaScript with accessibility as a fundamental part of the process.

This project is in the process of being built. At some point soon it will be ready to show the world.

## So what's a11y.build?
For now, the plan is to create the site as a series of lessons that teach the fundamentals of HTML, CSS, and JavaScript as though all of the most important accessibility features were necessary to make a site work properly because, when you think about it for a second, _they are necessary to make a site work properly_.

The site will be composed of two top-level pages: the blog, and the guide. The idea is to post new content to the blog as I learn it, then refine it and make it a part of the guide.

Eventually the guide will begin to solidify enough that it can be treated as a book or a course on fundamental, a11y-centered development.

Following all of that I imagine I'll want to create a third section with accessible components and how to implement them.

## Why?

The CDC estimates that [26% of adults in the US have some type of disability](https://www.cdc.gov/ncbddd/disabilityandhealth/infographic-disability-impacts-all.html). While there's a moral imperative to provide access to the content we create, there's also a professional imperative — we should strive to create sites that work as close to 100% of the time as possible. If we're creating sites that don't work well for 26% of people, we're creating sites that only work 74% of the time.

And nobody likes skating by with a C average, right?

## Outline
a11y.build will be composed of two major approaches to the content. 

The first, a guide to creating HTML documents from the ground up, presented as a series of lessons that go into the necessary steps for the creation of a website following accessible practices.

The second, a collection of posts and tutorials that walk through the practical implementation of a given topic in a friendly way.

There may also be two additional sections — Accessible Components, and Further Information (or something like that).

Accessible Components will be devoted to providing installable packages that coincide with a tutorial on how to build the component following accessible practices.

Further Information will be devoted to tangential information related to a given portion of the guide. For example: a post exploring the history of how HTML was created that's linked to from inside the guide's HTML introduction. (this may be too much, but at the moment it feels like it could be important to include information about how this platform came to be and the various protocols and APIs that make it function)

I may follow the [Diátaxis](https://diataxis.fr/) documentation framework and present the tutorials first. I'm really not sure yet.

1. Introduction
   1. What is HTML? -> History of HTML
   2. (more stuff, obviously)