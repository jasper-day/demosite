---
title: Lattice 3D Model
---


There is a massive, open-source [repository of crystal information called the COD](https://www.crystallography.net/cod/browse.html), but it seems like a decent amount of work would need to be done to turn the models mosted there into something that would be instantly useful to a student using the MatLib website.

In particular:

- Create web tooling to allow easy phone interfacing to JSmol (displaying default as unit cell, making common commands into buttons)
- Write scripts to make it easier to actually find the desired crystal (SQL querying and hand search is *not* going to cut it for 100s of materials!)


All the information there is stored in Crystallographic Information Files ([CIF](https://en.wikipedia.org/wiki/Crystallographic_Information_File)), which can be directly read by JSmol. All you have to do is direct JSmol to display the right crystal!

Test: [simple](simple.md)

This information can be embedded on a webpage using [**JSmol**](https://wiki.jmol.org/index.php/Jmol_PHP):

<script type="text/javascript" src="../lib/jsmol/JSmol.min.js"></script>

<script type="text/javascript"> 
    
    $(document).ready(function() { 
    /*
    })
    $$
    */
    Info = {
    	width: 400,
    	height: 400,
    	debug: false,
    	j2sPath: "../lib/jsmol/j2s",
    	color: "0xEEEEEE",
      disableJ2SLoadMonitor: true,
      disableInitialConsole: false,
    	// addSelectionOptions: true,
    	serverURL: "https://chemapps.stolaf.edu/jmol/jsmol/php/jsmol.php",
    	use: "HTML5",
    	readyFunction: null,
    	script: "load ../assets/5000217.cif {444 666 1} + Display 555"
    }
    
    $("#mydiv").html(Jmol.getAppletHtml("jmolApplet0",Info)) 
    /*
    $$
    ({ pay no attention to the man behind the curtain
    */
    });
    
</script>

<span id=mydiv></span>

<a href="javascript:Jmol.script(jmolApplet0, 'load ../assets/9008469.cif {444 666 1} + Display 555')">Face Centered Cubic</a>

<a href="javascript:Jmol.script(jmolApplet0, 'load ../assets/5000217.cif {444 666 1} + Display 555')">Body Centered Cubic</a>



<a href="javascript:Jmol.script(jmolApplet0, 'spin on')">spin on (MD, fixed?)</a>

<a href="javascript:Jmol.script(jmolApplet0, 'spin off')">spin off (fixed??)</a>

