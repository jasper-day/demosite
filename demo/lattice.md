---
title: Lattice 3D Model
---


There is a massive, open-source [repository of crystal information called the COD](https://www.crystallography.net/cod/browse.html), but it seems like a decent amount of work would need to be done to turn the models mosted there into something that would be instantly useful to a student using the MatLib website.

All the information there is stored in Crystallographic Information Files ([CIF](https://en.wikipedia.org/wiki/Crystallographic_Information_File)) which contain the dimensions and angles of a unit cell of the crystal (but this is confusing, and it seems like most of the results are for complicated research crystals!)

Test: [simple](simple.md)

This information can be embedded on a webpage using [**JSmol**](https://wiki.jmol.org/index.php/Jmol_PHP):

<script type="text/javascript" src="../lib/jsmol/JSmol.min.js"></script>

<script type="text/javascript"> 
    $(document).ready(function() { 
    
    Info = {
    	width: 400,
    	height: 400,
    	debug: false,
    	j2sPath: "../lib/jsmol/j2s",
    	color: "0xC0C0C0",
      disableJ2SLoadMonitor: true,
      disableInitialConsole: true,
    	addSelectionOptions: true,
    	serverURL: "https://chemapps.stolaf.edu/jmol/jsmol/php/jsmol.php",
    	use: "HTML5",
    	readyFunction: null,
    	script: "load $caffeine"
    }
    
    $("#mydiv").html(Jmol.getAppletHtml("jmolApplet0",Info)) 
    
    });
    
</script>

<span id=mydiv></span>
<a href="javascript:Jmol.script(jmolApplet0, 'spin on')">spin on</a>

<a href="javascript:Jmol.script(jmolApplet0, 'spin off')">spin off</a>