# calculator-made-easy


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <title> Calculator </title>
<style>
.container{
    text-align: center;
    margin-top:  25px;
}
table{
    margin:auto;
}

input{
    border-radius: 21px;
    border: 20px solid #798fbe;
    font-size:34px;
    height: 65px;
    width: 456px;
}

button{
 background: chartreuse;
 border-radius: 40px;
 font-size: 40px;
 width: 102px;
    height: 90px;
    margin: 6px;
}
.calculator{
    border: 4px solid #0feb3f60;
    background-color: #0a0a0a;
    padding: 23px;
    border-radius: 53px;
    display: inline-block;
}
h1{
    font-size: 48px;
    font-family: 'Courier New', Courier, monospace;
}
body{
    background-image: url('https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQPpXYf1nqgjroWtc_ZtJjpY3VjuHp_JZkiTA&usqp=CAU');
background-size: 100%;
}
p{
    font-size: 30px;
}
    p {
    animation-duration: 5s;
    animation-name: slidein;
  }
  
  @keyframes slidein {
    from {
      font-size: 150%;
         margin-left: 100%;
      width: 300%;
    }
  
    
  
    to {
      font-size: 150%;
      margin-left: 0%;
      width: 100%;
    }
  }
</style>
</head>
<body>
    <p>Calculator Made BY Manan Gupta..</p>
    <div class="container">
    <h1> Calculator By Manan</h1>

    <div class="calculator">
    <input type="text" name="screen" id="screen">
    <table>
        <tr>
            <td><button>(</button></td>
            <td><button>)</button></td>
            <td><button style="background-color:rgb(240, 8, 124);">C</button></td>
            <td><button>%</button></td>
        </tr>
        <tr>
            <td><button>7</button></td>
            <td><button>8</button></td>
            <td><button>9</button></td>
            <td><button>X</button></td>
        </tr>
        <tr>
            <td><button>4</button></td>
            <td><button>5</button></td>
            <td><button>6</button></td>
            <td><button>-</button></td>
        </tr>
        <tr>
            <td><button>1</button></td>
            <td><button>2</button></td>
            <td><button>3</button></td>
            <td><button>+</button></td>
        </tr>
        <tr>
            <td><button>0</button></td>
            <td><button>.</button></td>
            <td><button>/</button></td>
            <td><button style="background-color:rgb(240, 8, 124);">=</button></td>
        </tr>
    </table>
</div>
</div>
</body>
<script>

console.log("calc using js");
let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText)
   if(buttonText == 'X'){
       buttonText = '*';
       screenValue += buttonText;
       screen.value = screenValue;
   }
   else if(buttonText == 'C'){
    screenValue = "";
    screen.value = screenValue;
 }
    else if(buttonText == '='){
        screen.value = eval(screenValue);
    }
    else {  
        screenValue += buttonText;
        screen.value = screenValue;
    }
    
    })
}
</script>
</html>
