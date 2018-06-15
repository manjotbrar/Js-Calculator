# Js-Calculator
<p> Manjot's Calculator<p>
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <iframe src="http://free.timeanddate.com/clock/i6a3u2vu/n188/bat5/tt0/tw0/tm1/ts1/tb4" frameborder="0" width="89" height="38"></iframe>

<div class="container">
	<fieldset id="container">
		<form name="calculator">
   <input type="button" id="AUTO" class="bigButton" value="AUTO" onclick="doAutoFlip();">
   <input type="button" id="STOP" class="bigButton " value="STOP " onclick="stopFlip(); ">
      			<input class="button digits mys" type="button" value="👀" onclick="calculator.display.value += '👀'">
			<input id="display" type="text" name="display" readonly>
      

      <input class="button digits" type="button" value="7" onclick="calculator.display.value += '7'">
			<input class="button digits" type="button" value="8" onclick="calculator.display.value += '8'">
			<input class="button digits" type="button" value="9" onclick="calculator.display.value += '9'">
			<input class="button mathButtons" type="button" value="+" onclick="calculator.display.value += ' + '">
			<br>
			<input class="button digits" type="button" value="4" onclick="calculator.display.value += '4'">
			<input class="button digits" type="button" value="5" onclick="calculator.display.value += '5'">
			<input class="button digits" type="button" value="6" onclick="calculator.display.value += '6'">
			<input class="button mathButtons" type="button" value="-" onclick="calculator.display.value += ' - '">
			<br>
			<input class="button digits" type="button" value="1" onclick="calculator.display.value += '1'">
			<input class="button digits" type="button" value="2" onclick="calculator.display.value += '2'">
			<input class="button digits" type="button" value="3" onclick="calculator.display.value += '3'">
			<input class="button mathButtons" type="button" value="x" onclick="calculator.display.value += ' * '">
			<br>
			<input id="clearButton" class="button" type="button" value="C" onclick="calculator.display.value = ''">
			<input class="button digits" type="button" value="0" onclick="calculator.display.value += '0'">
			<input class="button mathButtons" type="button" value="=" onclick="calculator.display.value = eval(calculator.display.value)">
			<input class="button mathButtons" type="button" value=" ÷" onclick="calculator.display.value += ' / '"> 
		</form>
 
    <script>
         
        var t = 0;
        var colour = 0;
        var checkStop = 0;
        var light = new Array();
        light[0] = 'yellow';
        light[1] = 'white';
        light[2] = 'light blue';
        light[3] = 'violet';
        light[4] = 'light purple';
        light[5] = 'grey';
        light[6] = 'carbon red';
        light[7] = 'Aqua';
        light[8] = 'light green'
        light[9] = 'light pink'
        light[10]= 'orange'
        light[11]= 'maroon'
         light[12]= 'turquoise'

        function flip(whichway) {
            document.body.style.backgroundColor = light[whichway];
        }

        function doAutoFlip() {
            flip(colour);
            if (colour < light.length) {
                colour++;
            } else {
                colour = 0;
            }

            t = setTimeout("doAutoFlip()", 35);
        }

        function stopFlip() {
            clearTimeout(t);
            document.body.style.backgroundColor = '#99a869"';
        }
    </script>
        
        <script>
function AddFunction() {
  var x = document.getElementById("number1").value;
  var y = document.getElementById("number2").value;
  if (x == y) {
        </script>
        
        <script>
} document.getElementById("result").innerHTML = "The result is : " + (Number(x) + Number(y)) * 3;
  } else
    document.getElementById("result").innerHTML = "The result is : " + (Number(x) + Number(y));


function SubtractFunction() {
  var x = document.getElementById("number1").value;
  var y = document.getElementById("number2").value;
  if (x == y) {
    document.getElementById("result").innerHTML = "The result is : " + (Number(x) - Number(y)) * 3;
  } else
    document.getElementById("result").innerHTML = "The result is : " + (Number(x) - Number(y));
}

function MultiplyFunction(){
        num1 = document.getElementById("number1").value;
        num2 = document.getElementById("number2").value;
        document.getElementById("result").innerHTML = num1 * num2;
}

function DivideFunction() { 
        num1 = document.getElementById("number1").value;
        num2 = document.getElementById("number2").value;
document.getElementById("result").innerHTML = num1 / num2;
}
    </script>
        
         <style>
             
         body {;
 background-color: lightblue;
font-family: fantasy;
}
.container {
	display: flex;
	align-items: center;
	justify-content: center;
}
#container {
	width: 285px
	padding: 8px 10px 10px 8px;
	margin: 10px auto;
	background-color: #424592;
	border-radius: 8px;
	border-top: 10px solid #C1C1C1;
	border-right: 2px solid #FFF;
	border-bottom: 10px solid #C1C1C1;
	border-left: 5px solid #C1C1C1;
	box-shadow: 2px 3px 7px rgba(0, 0, 0,), inset -100px 0px 100px 
}

#display {
	display: block;
	margin: 15px auto;
	height: 55px;
	width: 174px;
	padding: 0 20px;
	border-radius: 4px;
	border-top: 4px solid #C1C1C1;
	border-right: 2px solid #C1C1C1;
	border-bottom: 2px solid #FFF;
	border-left: 2px solid #FFF;
	background-color: #FFF;
	box-shadow: inset 2px 0px 10px #030303, inset 0px -20px 1px rgba(150, 150, 150, .2);
	font-size: 28px;
	color: #666;
	text-align: right;
	font-weight: 400;
}

.button {
	display: inline-block;
	margin: 10px;
	width: 40px;
	height: 35px;
	font-weight: bold;

}

.mathButtons {
	margin: 4px 10px  1px;
	color: #FFF;
	text-shadow: -1px -1px 0px #44006F;
	border-bottom: 2px solid #181818;
	border-left: 1px solid #181818;
	box-shadow: 0px 2px 2px #030303, inset 0px -20px 1px #2E2E2E;
}

.digits {
	color: #181818;
	text-shadow: 1px 1px 0px #FFF;
	background-color: #EBEBEB;
	border-top: 2px solid #FFF;
	border-bottom: 2px solid #C186C1;
	border-left: 2px solid #C1C1C1;
	border-radius: 4px;
	box-shadow: 0px 0px 2px #035603, inset 0px -20px 1px #DCDCDC;
}

.digits:hover,
.mathButtons:hover,
#clearButton:hover {
}

#clearButton {
background-color: #D20500;
	box-shadow: 0px 0px 2px #030303, inset 0px -20px 1px #B00000;
}

.mys {
  float:right;
  margin: -3px
}
         </style>
