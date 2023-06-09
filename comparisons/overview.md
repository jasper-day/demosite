---
title: MatLib Website Options
---

All options open-source.
 
1. Static serving with markdown pages (like this!)
    - Pros:
        - Extremely self evident. Simply write new markdown files
        - Easily transfer stewardship
        - Can be upgraded later; markdown is ridiculously versatile and ubiquitous
    - Cons:
        - no LaTeX equations
        - General limited functionality and more work done by hand
        - less customizable out of the box
2. Static serving with [Quarto](https://quarto.org/)
    - Quarto is the latest evolution of R markdown, allowing all-in-one site generation while still basically usinhg markdown files.
    - Pros:
        - Familiar and comfortable
        - Extremely powerful and flexible
        - Great tooling (VSCode extension) makes life easy
        - Fully featured
    - Cons:
        - Requires new steward to learn the system, slightly less obvious
        - Although integration is generally painless, site generation can occasionally break for obscure reasons especially when code is involved, or when filenames conflict.
        - Newer and less stable
3. Graphical serving with [WikiJS](https://js.wiki/)
    - Pros:
        - Very "friendly" once it's working: feels like a modern website, with material design, user accounts, etc
        - Markdown or visual editor
        - Nice administrative tools
        - No git experience required
    - Cons:
        - Least flexible approach
        - Fewer options than Quarto
        - Not as pretty or customizable
        - Overkill (in my opinion, of course)
4. [**Grav**](http://68.183.46.43:8080)
    - Pros:
        - Files stored as Markdown locally on the machine
        - Easy to set up
        - Highly customizable online interface allows online content generation, like WikiJS
        - Extensible with plugins to display 3D models, JSmol, etc etc etc
        - More functionality than a static website like Quarto
        - No database
    - Cons:
        - No database (if that's a con for you)
