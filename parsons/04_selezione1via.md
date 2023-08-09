---
layout: default
title: Selezione 1 via
---
## Selezione 1 via (Somma due numeri)
<div id="04_selezione1via-sortableTrash" class="sortable-code"></div> 
<div id="04_selezione1via-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="04_selezione1via-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="04_selezione1via-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "print(&quot;Ciao! Facciamo il controllo della somma.&quot;)\n" +
    "addendo1 = int(input(&quot;Inserisci il primo addendo: &quot;))\n" +
    "addendo2 = int(input(&quot;Inserisci il secondo addendo: &quot;))\n" +
    "somma = addendo1 + addendo2\n" +
    "if (somma &gt;= 10):\n" +
    "    print(&quot;la somma e&#039; maggiore o uguale a 10&quot;)\n" +
    "    if (somma &lt;= 15):\n" +
    "        print(&quot;la somma e&#039; compresa tra 10 e 15&quot;)\n" +
    "print(&quot;Ciao, alla prossima!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "04_selezione1via-sortable",
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
  $("#04_selezione1via-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#04_selezione1via-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>