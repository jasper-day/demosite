---
title: Super simple JSmol
---

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