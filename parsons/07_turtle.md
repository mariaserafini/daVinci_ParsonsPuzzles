<div id="07_turtle-sortableTrash" class="sortable-code"></div> 
<div id="07_turtle-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="07_turtle-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="07_turtle-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "import turtle\n" +
    "turtle.pencolor(&quot;cyan&quot;)\n" +
    "turtle.fillcolor(&quot;magenta&quot;)\n" +
    "turtle.begin_fill()\n" +
    "turtle.forward(200)\n" +
    "turtle.left(120)\n" +
    "turtle.forward(200)\n" +
    "turtle.left(120)\n" +
    "turtle.forward(200)\n" +
    "turtle.left(120)\n" +
    "turtle.end_fill()";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "07_turtle-sortable",
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
  $("#07_turtle-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#07_turtle-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>