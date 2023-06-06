---
title: Lattice 3D Model
---


There is a massive, open-source [repository of crystal information called the COD](https://www.crystallography.net/cod/browse.html), but it seems like a decent amount of work would need to be done to turn the models mosted there into something that would be instantly useful to a student using the MatLib website.

All the information there is stored in Crystallographic Information Files ([CIF](https://en.wikipedia.org/wiki/Crystallographic_Information_File)) which contain the dimensions and angles of a unit cell of the crystal (but this is confusing, and it seems like most of the results are for complicated research crystals!)

This information can be embedded on a webpage using [**JSmol**](https://wiki.jmol.org/index.php/Jmol_PHP):

<div id="JmolDiv" style="width: 30vw, height: 30vw"></div>

<script type="text/javascript" src="../jsmol/jsmol/JSmol.min.js"></script>

<script type="text/javascript">
    var myJmol = 'myJmol';
    var Info = {
        width: "100%",
        height: "100%",
        color: "#FFFFFF",
        serverURL: "../jsmol/jsmol/php/jsmol.php",
        j2sPath: "../jsmol/jsmol/j2s",
        script: "load DATA https://www.crystallography.net/cod/4313209.cif@201982",
    }
    $(document).ready(function(){
        Jmol.script(myJmol, 'load ../model/caffeine.xyz');
        $('#JmolDiv').html( Jmol.getAppletHtml(myJmol, Info) );
        });
        
</script>