# Javascript-calculator
<!DOCTYPE html>
<html>
<head>
	<title>Calculator</title>
	<meta name="first javascript project" content="Simple calculator"/>
<link rel="stylesheet" type="text/css" href="style.css">
<script type="text/javascript" src="script.js"></script>
</head>
<body>

<div class="container">
	<div class="calc-container">

		<h1>Calculator</h1>

		<input id="box" value="" type="text" readonly placeholder="0"><br/>
       
         <!-- my buttons below -->

		<div class="btn-container">
		<div class="row">
				<button class="btn" onclick="shownum('1')"><strong>1</strong></button>
				<button class="btn" onclick="shownum('2')"><strong>2</strong></button>
				<button class="btn" onclick="shownum('3')"><strong>3</strong></button>
				<button class="btn cbtn" onclick="delback()"><strong>del</strong></button>
		</div>
		<div class="row">
				<button class="btn" onclick="shownum('4')"><strong>4</strong></button>
				<button class="btn" onclick="shownum('5')"><strong>5</strong></button>
				<button class="btn" onclick="shownum('6')"><strong>6</strong></button>
				<button class="btn" onclick="shownum('+')"><strong>+</strong></button>
		</div>
		<div class="row">
				<button class="btn" onclick="shownum('7')"><strong>7</strong></button>
				<button class="btn" onclick="shownum('8')"><strong>8</strong></button>
				<button class="btn" onclick="shownum('9')"><strong>9</strong></button>
				<button class="btn" onclick="shownum('-')"><strong>-</strong></button>
		</div>
		<div class="row">
				<button class="btn" onclick="shownum('.')"><strong>.</strong></button>
				<button class="btn" onclick="shownum('0')"><strong>0</strong></button>
				<button class="btn" onclick="shownum('00')"><strong>00</strong></button>
				<button class="btn" onclick="shownum('*')"><strong>*</strong></button>
				
		</div>
		<div class="row">
				<button class="btn cbtn" onclick="clearme()"><strong>C</strong></button>
				<button class="btn solvebtn" onclick="solve()"><strong>=</strong></button>
				<button class="btn" onclick="shownum('/')"><strong>/</strong></button>
		</div>	
		
		</div>


	</div>
</div>

	<footer id="footer">Designed by Odagboyi frieda <a  target="_blank" style="color: palevioletred"></a></footer>
</body>
</html>



<!-- my css code -->

h1 {color: #fff;}
.container{
        margin: 0 auto;
        }  
.calc-container {
		padding: 20px;
		background: palevioletred;
		width: 250px;
		border-radius: 20px;
		box-shadow: 10px 10px 5px #888888;	   
		-moz-box-shadow: 10px 10px 5px #888888;
		-webkit-box-shadow: 10px 10px 5px #888888;
		margin: 10px auto;
        }
#box {
        width:100%; 
        height: 40px; 
        border:1px solid #000; 
        background: #ddded9; 
        font-size: 30px; 
        text-align: right;
        color:rgb(156, 65, 65);
		margin: 0 auto;
	
        } 
.btn-container {
		margin: 10px 5px;
		background:beige;
}

.btn {
		height: 40px;
		width: 40px;
        padding: 10px; 
		background: black; 
        color: #fff; 
		border: none;
        margin: 8px; 
        font-size: 15px;    
		box-shadow: 1px 1px 1px #000;
	    -moz-box-shadow: 1px 1px 1px #000;
	    -webkit-box-shadow: 1px 1px 1px #000;
        }

.btn:hover {background-color: #000}

.btn:active {
  background-color: #000;
  box-shadow: 0 5px #666;
  transform: translateY(2px);
}
.solvebtn {
		width:100px;
		background:palevioletred;
}
.solvebtn:hover {background-color: black;}

.solvebtn:active {
  background-color: #013e01;
  box-shadow: 0 5px #666;
  transform: translateY(2px);
}
.cbtn {
		background: rgb(42, 86, 114); 
}
.cbtn:hover {background-color: palevioletred}

.cbtn:active {
  background-color: palevioletred;
  box-shadow: 0 5px #666;
  transform: translateY(2px);
}
#footer {
		position:fixed;
	   	left:0px;
	   	bottom:0px;
	   	height:10px;
	   	width:100%;
	   	background:#000;
		text-align: center;
		margin: 0px auto;
		padding: 10px;
		color: #fff;
		}
#footer a:link {color: #fff;text-decoration: none;}



<!--my javascript code  -->
// Get the Variable from the input box
function screen(val)
        {
        document.getElementById("box").value=val;
        }

// Concatenating Values
function shownum(val)   {
        document.getElementById("box").value+=val;
        }

// Performing the Calcuulation
function solve() { 
    try     { 
            screen(eval(document.getElementById("box").value)) 
            } 
    catch(e) {
            screen('Error') 
            } 
                 }
// Clear the Input Screen
function clearme() {
                document.getElementById("box").value = "";
                } 
// Backspace Function
function delback() {
                var valueNeeded = document.getElementById("box").value;
                var finalValueNeeded = valueNeeded.substr(0, valueNeeded.length-1); 
                document.getElementById("box").value=finalValueNeeded;
                
                } 
