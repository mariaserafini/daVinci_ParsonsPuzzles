---
layout: default
title: Page 2 Example (Variable Check Grader)
---

## Selezione a 3 vie (Ristorante)
Metti in ordine le seguenti linee di codice 
<div id="06_selezione3vie-sortableTrash" class="sortable-code"></div> 
<div id="06_selezione3vie-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="06_selezione3vie-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="06_selezione3vie-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "print(&quot;Ciao. Benvenuto in questo ristorante&quot;)\n" +
    "s = input(&quot;Ordiniamo. Vuoi la pasta o la pizza? &quot;)\n" +
    "if s == &quot;pizza&quot;:\n" +
    "    t = input(&quot;margherita o funghi? &quot;)\n" +
    "    if t == &quot;margherita&quot;:\n" +
    "        print(&quot;Costo margherita: 5 euro&quot;)\n" +
    "    elif t == &quot;funghi&quot;:\n" +
    "        print(&quot;Costo funghi: 6 euro&quot;)\n" +
    "elif s == &quot;pasta&quot;:\n" +
    "    t = input(&quot;carbonara o amatriciana?&quot;)\n" +
    "    if t == &quot;carbonara&quot;:\n" +
    "        print(&quot;Costo carbonara: 7 euro&quot;)\n" +
    "    elif t == &quot;amatriciana&quot;:\n" +
    "        print(&quot;Costo amatriciana: 7.50 euro&quot;)\n" +
    "else:\n" +
    "    print(&quot;Input scorretto&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "06_selezione3vie-sortable",
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
  $("#06_selezione3vie-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#06_selezione3vie-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
