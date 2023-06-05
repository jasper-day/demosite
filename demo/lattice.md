---
title: Lattice 3D Model
---


There is a massive, open-source [repository of crystal information called the COD](https://www.crystallography.net/cod/browse.html), but it seems like a decent amount of work would need to be done to turn the models mosted there into something that would be instantly useful to a student using the MatLib website.

All the information there is stored in Crystallographic Information Files ([CIF](https://en.wikipedia.org/wiki/Crystallographic_Information_File)) which contain the dimensions and angles of a unit cell of the crystal (but this is confusing, and it seems like most of the results are for complicated research crystals!)

This information can be embedded on a webpage using [**JSmol**](https://wiki.jmol.org/index.php/Jmol_PHP):


<script type="text/javascript" src="https://chemapps.stolaf.edu/jmol/jsmol/JSmol.min.js"></script>

<script type="text/javascript">
    window.addEventListener("DOMContentLoaded", function () {
        var jmolApplet = Jmol.getApplet("jmolApplet", {
            width: "40vw",
            height: "40vw",
            serverURL: "https://chemapps.stolaf.edu/jmol/jsmol/php/jsmol.php",
            j2sPath: "https://chemapps.stolaf.edu/jmol/jsmol/j2s",
            script: "load inline https://www.crystallography.net/cod/4313209.cif@201982",
        });
    });
</script>

<div id="jmolApplet"></div>
