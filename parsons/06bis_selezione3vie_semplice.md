<div id="06bis_selezione3vie_semplice-sortableTrash" class="sortable-code"></div> 
<div id="06bis_selezione3vie_semplice-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="06bis_selezione3vie_semplice-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="06bis_selezione3vie_semplice-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "print(&quot;Ciao. Benvenuto a teatro!&quot;)\n" +
    "risposta=int(input(&quot;Quanti anni hai? &quot;))\n" +
    "if risposta&lt;=14:\n" +
    "    print(&quot;Hai diritto alla riduzione Junior!&quot;)\n" +
    "elif risposta&gt;=65:\n" +
    "    print(&quot;Hai diritto alla riduzione Senior!&quot;)\n" +
    "else:\n" +
    "    print(&quot;Devi pagare il biglietto intero.&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "06bis_selezione3vie_semplice-sortable",
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
  $("#06bis_selezione3vie_semplice-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#06bis_selezione3vie_semplice-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>