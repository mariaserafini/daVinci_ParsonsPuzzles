<div id="10_sqlBase2.md-sortableTrash" class="sortable-code"></div> 
<div id="10_sqlBase2.md-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="10_sqlBase2.md-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="10_sqlBase2.md-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "SELECT *
\n" +
    "FROM studenti
\n" +
    "WHERE nazione=&#039;Italia&#039;
\n" +
    "AND nazione=&#039;USA&#039;
\n" +
    "ORDER BY cognome
\n" +
    "LIMIT 5";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "10_sqlBase2.md-sortable",
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
  $("#10_sqlBase2.md-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#10_sqlBase2.md-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
