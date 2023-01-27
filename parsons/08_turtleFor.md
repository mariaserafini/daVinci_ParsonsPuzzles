<div id="08_turtleFor-sortableTrash" class="sortable-code"></div> 
<div id="08_turtleFor-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="08_turtleFor-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="08_turtleFor-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "import turtle\n" +
    "turtle.penup()\n" +
    "turtle.goto(-100,-100)\n" +
    "turtle.pendown()\n" +
    "turtle.fillcolor(&quot;orange&quot;)\n" +
    "turtle.begin_fill()\n" +
    "for contatore in range(6):\n" +
    "    turtle.forward(100)\n" +
    "    turtle.left(360/6)\n" +
    "turtle.end_fill()\n" +
    "turtle.write(&quot;ho disegnato un esagono!&quot;)";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "08_turtleFor-sortable",
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
  $("#08_turtleFor-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#08_turtleFor-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>