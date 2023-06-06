---
title: Lattice 3D Model
---


There is a massive, open-source [repository of crystal information called the COD](https://www.crystallography.net/cod/browse.html), but it seems like a decent amount of work would need to be done to turn the models mosted there into something that would be instantly useful to a student using the MatLib website.

All the information there is stored in Crystallographic Information Files ([CIF](https://en.wikipedia.org/wiki/Crystallographic_Information_File)) which contain the dimensions and angles of a unit cell of the crystal (but this is confusing, and it seems like most of the results are for complicated research crystals!)

Test: [simple](simple.md)

This information can be embedded on a webpage using [**JSmol**](https://wiki.jmol.org/index.php/Jmol_PHP):

<div id="JmolDiv" style="width: 30vw, height: 30vw"></div>

<script type="text/javascript" src="lib/jsmol/JSmol.min.js"></script>

<script type="text/javascript">
    var myJmol = 'myJmol';
    var Info = {
        width: "100%",
        height: "100%",
        color: "#FFFFFF",
        j2sPath: "lib/jsmol/j2s",
        script: "load ./assets/5000217.cif {444,555,666}",
    }
    $(document).ready(function(){
        Jmol.script(myJmol, "load ./assets/5000217.cif");
        $('#JmolDiv').html( Jmol.getAppletHtml(myJmol, Info) );
        });
        
</script>