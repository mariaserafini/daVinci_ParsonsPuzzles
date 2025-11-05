<div id="11_slqGroup-sortableTrash" class="sortable-code"></div> 
<div id="11_slqGroup-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="11_slqGroup-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="11_slqGroup-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "SELECT MAX(prezzo)\n" +
    "FROM automobili\n" +
    "WHERE prezzo &gt;40000\n" +
    "AND tipo = &#039;4x4&#039;\n" +
    "GROUP BY marca\n" +
    "ORDER BY prezzo ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "11_slqGroup-sortable",
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
  $("#11_slqGroup-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#11_slqGroup-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>