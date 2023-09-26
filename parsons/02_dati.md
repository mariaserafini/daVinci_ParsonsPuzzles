---
layout: default
title: Tipi di dato
---
## Tipi di dato (Fruttivendolo)

<div id="02_dati-sortableTrash" class="sortable-code"></div> 
<div id="02_dati-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="02_dati-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="02_dati-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "print(&quot;inserire prezzo meloni al pezzo&quot;)\n" +
    "prezzo = float(input())\n" +
    "print(&quot;inserire numero meloni acquistati&quot;)\n" +
    "numero = int(input())\n" +
    "totale = prezzo * numero\n" +
    "print(&quot;devi pagare&quot;,totale,&quot;euro&quot;)\n" +
    "print(&quot;inserire importo banconota&quot;)\n" +
    "banconota = int(input())\n" +
    "resto = banconota - totale\n" +
    "print(&quot;Otterrai di resto &quot;,resto,&quot;euro&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "02_dati-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#02_dati-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#02_dati-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>