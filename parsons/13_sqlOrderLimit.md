<div id="13_sqlOrderLimit-sortableTrash" class="sortable-code"></div> 
<div id="13_sqlOrderLimit-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="13_sqlOrderLimit-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="13_sqlOrderLimit-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "SELECT *\n" +
    "FROM studenti\n" +
    "WHERE nazione=&#039;Italia&#039;\n" +
    "AND nazione=&#039;USA&#039;\n" +
    "ORDER BY cognome\n" +
    "LIMIT 5";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "13_sqlOrderLimit-sortable",
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
  $("#13_sqlOrderLimit-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#13_sqlOrderLimit-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
