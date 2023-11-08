<div id="09_file-sortableTrash" class="sortable-code"></div> 
<div id="09_file-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="09_file-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="09_file-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "file = open(&#039;libri.txt&#039;, &#039;r+&#039;)\n" +
    "testo = file.readlines()\n" +
    "x = 0\n" +
    "for riga in testo:\n" +
    "   x = x + 1\n" +
    "   print(&quot;Riga&quot;,x,&quot;:&quot;,riga)\n" +
    "file.write(&quot;ultimo libro&quot;)\n" +
    "file.close()";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "09_file-sortable",
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
  $("#09_file-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#09_file-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>