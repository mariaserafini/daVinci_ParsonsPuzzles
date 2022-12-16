---
layout: default
title: Selezione a 2 vie
---
## Selezione a 2 vie (Media voti)
<div id="05_selezione2vie-sortableTrash" class="sortable-code"></div> 
<div id="05_selezione2vie-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="05_selezione2vie-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="05_selezione2vie-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "print(&quot;Ciao! Controlliamo come va in informatica&quot;)\n" +
    "voto1 = float(input(&quot;inserisci il primo voto che hai preso&quot;))\n" +
    "voto2 = float(input(&quot;inserisci il secondo voto che hai preso&quot;))\n" +
    "media = (voto1+voto2)/2\n" +
    "if media &gt;= 6:\n" +
    "    print(&quot;benissimo! Procedi cosi&#039;!&quot;)\n" +
    "else:\n" +
    "    if voto2 &gt; voto1:\n" +
    "        print(&quot;bene! Almeno stai migliorando!&quot;)\n" +
    "    else:\n" +
    "        print(&quot;Bisogna recuperare!!&quot;)\n" +
    "print(&quot;A presto.&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "05_selezione2vie-sortable",
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
  $("#05_selezione2vie-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#05_selezione2vie-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>