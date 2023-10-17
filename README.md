1<html>
<body style="background-color:powderblue;">
     
        <h1 style="font-size:300%;"><h1 style="font-family:verdana;"><h1 style="text-align:center;"><p id="text" onclick="func()">
    <b>&#128151;Matchmaker for the Web&#128151;</b>
    <p>Cupid's Favorite Game</p>

<h2 style="font-size:100%;"><i>It might not be month of love, but love will always be around us whether it's romantic or platonic. This quiz determines what you and I are meant to be. Friends? Foes? Lovers? Don't worry it's not too long, just five simple questions. If you very strongly agree with the statement I present to you answer a 5, if you just agree answer a 4, if you are indifferent answer a 3, if you disagree answer a 2 & if you very strongly disagree with what I have presented to you then answer a 1. So take a chance and let us gamble with the fates.</i></h2>

     <label>Technoblade is the greatest streamer of all time.</label><br />
	<select id="q1">
          <option value="5">Very Strongly Agree</option>
		<option value="4">Agree</option>
		<option value="3">Neutral</option>
		<option value="2">Disagree</option>
		<option value="1">Very Strongly Disagree</option>
     </select>
     <br /><br />

     <label>Lovejoy makes pretty good music.</label><br />
     	<select id="q2">
          <option value="5">Very Strongly Agree</option>
		<option value="4">Agree</option>
		<option value="3">Neutral</option>
		<option value="2">Disagree</option>
		<option value="1">Very Strongly Disagree</option>
     </select>
     <br /><br />

     <label>Cats are better than dogs.</label><br />
     	<select id="q3">
         	 <option value="5">Very Strongly Agree</option>
		<option value="4">Agree</option>
		<option value="3">Neutral</option>
		<option value="2">Disagree</option>
		<option value="1">Very Strongly Disagree</option>
     </select>
     <br /><br />

<label>Reading is a fun thing to do.</label><br />
     	<select id="q4">
          	<option value="5">Very Strongly Agree</option>
		<option value="4">Agree</option>
		<option value="3">Neutral</option>
		<option value="2">Disagree</option>
		<option value="1">Very Strongly Disagree</option>
     </select>
     <br /><br />

     <label>I enjoy playing Minecraft.</label><br />
     	<select id="q5">
          <option value="5">Very Strongly Agree</option>
		<option value="4">Agree</option>
		<option value="3">Neutral</option>
		<option value="2">Disagree</option>
		<option value="1">Very Strongly Disagree</option>
     </select>
     <br /><br />

	<br /><br /><br />
	<button onclick="submit()">Submit</button>
	<p id="submit"></p>

<script>
console.log("Starting Matchmaker Lite...");

function submit() {
	console.log("submit()");

	document.getElementById("submit").innerHTML = "Your compatibility is...";
}

</script>
