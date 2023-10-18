<html>
<body style="background-color:powderblue;">
     
        <h1 style="font-size:300%;"><h1 style="font-family:verdana;"><h1 style="text-align:center;"><p id="text" onclick="func()">
    <b>&#128151;Matchmaker for the Web&#128151;</b>
    <p>Cupid's Favorite Game</p>

<h2 style="font-size:100%;"><i>It might not be month of love, but love will always be around us whether it's romantic or platonic. This quiz determines what you and I are meant to be. Friends? Foes? Lovers? Don't worry it's not too long, just five simple questions. If you very strongly agree with the statement I present to you answer a 5, if you just agree answer a 4, if you are indifferent answer a 3, if you disagree answer a 2 & if you very strongly disagree with what I have presented to you then answer a 1. So take a chance and let us gamble with the fates.</i></h2>

     <label>Technoblade is the greatest streamer of all time.</label><br />
	<select id="q1">
          	<option value="5">5</option>
		<option value="4">4</option>
		<option value="3">3</option>
		<option value="2">2</option>
		<option value="1">1</option>
     </select>
     <br /><br />

     <label>Lovejoy makes pretty good music.</label><br />
     	<select id="q2">
          	<option value="5">5</option>
		<option value="4">4</option>
		<option value="3">3</option>
		<option value="2">2</option>
		<option value="1">1</option>
     </select>
     <br /><br />

     <label>Cats are better than dogs.</label><br />
     	<select id="q3">
                <option value="5">5</option>
		<option value="4">4</option>
		<option value="3">3</option>
		<option value="2">2</option>
		<option value="1">1</option>
     </select>
     <br /><br />

<label>Reading is a fun thing to do.</label><br />
     	<select id="q4">
          	<option value="5">5</option>
		<option value="4">4</option>
		<option value="3">3</option>
		<option value="2">2</option>
		<option value="1">1</option>
     </select>
     <br /><br />

     <label>I enjoy playing Minecraft.</label><br />
     	<select id="q5">
                <option value="5">5</option>
		<option value="4">4</option>
		<option value="3">3</option>
		<option value="2">2</option>
		<option value="1">1</option>
     </select>
     <br /><br />

	<br /><br /><br />
	<button onclick="submit()">Submit</button>
	<p id="submit"></p>

<script>
console.log("Starting Matchmaker Lite...");

function submit() {
	console.log("submit()");

	const DESIRED_RESPONSE = [
		5, /* 5 */
		2, /* 2 */
		1, /* 1 */
	]

	const MAX_SCORE = 25;

	let question1Response = document.getElementById("q1").selectedOptions[0].value;
	let question2Response = document.getElementById("q2").selectedOptions[0].value;
	let question3Response = document.getElementById("q3").selectedOptions[0].value;
	let question4Response = document.getElementById("q4").selectedOptions[0].value;
	let question5Response = document.getElementById("q5").selectedOptions[0].value;

	console.log("Question 1 Answers:")
	console.log(document.getElementById("q1").selectedOptions[0].text);
	console.log(document.getElementById("q1").selectedOptions[0].value);
	console.log(question1Response);

	console.log("Question 2 Answers:");
	console.log(document.getElementById("q2").selectedOptions[0].text);
	console.log(document.getElementById("q2").selectedOptions[0].value);
	console.log(question2Response);

	console.log("Question 3 Answers:");
	console.log(document.getElementById("q3").selectedOptions[0].text);
	console.log(document.getElementById("q3").selectedOptions[0].value);
	console.log(question3Response);

	// Todo: Calculate compatibility scores.
	let question1Compatibility = 5 - Math.abs(question1Response - DESIRED_RESPONSE[0]);
	let question2Compatibility = 5 - Math.abs(question2Response - DESIRED_RESPONSE[0]);
	let question3Compatibility = 5 - Math.abs(question3Response - DESIRED_RESPONSE[2]);

	console.log("c1="+question1Compatibility);
	console.log("c2="+question2Compatibility);
	console.log("c3="+question3Compatibility);

	// Calculate total compatibility. 
	let totalCompatibility = question1Compatibility + question2Compatibility + question3Compatibility;

	// Convert totalCompatibility to a percentage.
	totalCompatibility *= 100 / MAX_SCORE;
	totalCompatibility = Math.round(totalCompatibility);
	console.log("tc="+ totalCompatibility);

	document.getElementById("submit").innerHTML = "Your compatibility is: " + totalCompatibility;
}

</script>
