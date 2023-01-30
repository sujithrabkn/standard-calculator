# Design of a Standard Calculator

## AIM:

To design a web application for a standard calculator.

## DESIGN STEPS:

### Step 1:
Clone into the repository and create project.
### Step 2:
Make the necessary changes in settings.py.
### Step 3:
Create folders for html,css and js inside static.
### Step 4:
Code in the html program in calc.html, style.css and index.js.
### Step 5:
Runserver to get the simple calculator output.
### Step 6:
Validate the HTML and CSS code.
### Step 6:
Publish the website in the given URL.

## PROGRAM :

#In calc.html:
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <link rel="stylesheet" href="/static/css/style.css">
    <title>Calculator</title>
</head>
<body>
    <div class="container">
        <h1>Calculator</h1>

        <div class="calculator">
            <input type="text" name="screen" id="screen">
            <table>
                <tr>
                    <td><button>(</button></td>
                    <td><button>)</button></td>
                    <td><button>C</button></td>
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
                    <td><button>=</button></td>
                </tr>
            </table>
        </div>
    </div>
</body>
<script src="/static/js/index.js"></script>
</html>
```

#In style.css:
```
.container{
    text-align: center;
    margin-top:23px
}

table{
    margin: auto;
}

input{
    border-radius: 21px;
    border: 5px solid #244624;
    font-size:34px;
    height: 65px;
    width: 456px;
}

button{
    border-radius: 20px;
    font-size: 40px;
    background: #978fa0;
    width: 102px;
    height: 90px;
    margin: 6px;
}

.calculator{ 
    border: 4px solid #13695d;
    background-color: #75dbf5;
    padding: 23px;
    border-radius: 53px;
    display: inline-block;
    
}
h1{
    font-size: 28px;
    font-family: 'Courier New', Courier, monospace;
}
```

#In index.js:
```
let screen = document.getElementById('screen');
buttons = document.querySelectorAll('button');
let screenValue = '';
for (item of buttons) {
    item.addEventListener('click', (e) => {
        buttonText = e.target.innerText;
        console.log('Button text is ', buttonText);
        if (buttonText == 'X') {
            buttonText = '*';
            screenValue += buttonText;
            screen.value = screenValue;
        }
        else if (buttonText == 'C') {
            screenValue = "";
            screen.value = screenValue;
        }
        else if (buttonText == '=') {
            screen.value = eval(screenValue);
        }
        else {
            screenValue += buttonText;
            screen.value = screenValue;
        }

    })
}
```

## OUTPUT:

### calucator:
![81](https://user-images.githubusercontent.com/119477857/215442960-1cc5365a-47d9-499f-b11f-c8c8dd059971.jpg)



### validator:

![82](https://user-images.githubusercontent.com/119477857/215442998-279983ab-83fe-42de-a8e1-31a2bacbf513.jpg)


## Result:
The program for designing simple calculator using javascript is executed successfully.
