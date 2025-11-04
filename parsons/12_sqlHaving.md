<div id="12_slqHaving-sortableTrash" class="sortable-code"></div> 
<div id="12_slqHaving-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="12_slqHaving-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="12_slqHaving-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "SELECT COUNT(*), marca\n" +
    "FROM automobili\n" +
    "WHERE prezzo &gt;40000\n" +
    "AND marca IN (&#039;Audi&#039;, &#039;BMW&#039;, &#039;Volvo&#039;)\n" +
    "GROUP BY marca\n" +
    "HAVING COUNT(*) &gt; 5\n" +
    "ORDER BY prezzo ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "12_slqHaving-sortable",
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
  $("#12_slqHaving-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#12_slqHaving-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>