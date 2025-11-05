<div id="10_slqBase-sortableTrash" class="sortable-code"></div> 
<div id="10_slqBase-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="10_slqBase-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="10_slqBase-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "SELECT marca, modello\n" +
    "FROM automobili\n" +
    "WHERE prezzo &gt;40000\n" +
    "AND marca = &#039;Audi&#039;\n" +
    "ORDER BY prezzo ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "10_slqBase-sortable",
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
  $("#10_slqBase-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#10_slqBase-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>