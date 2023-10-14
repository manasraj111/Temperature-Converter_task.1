# Temperature-Converter_task.1

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Temperature Converter</title>
    <script src="https://kit.fontawesome.com/11c75dba75.js"
    crossorigin="anonymous"></script>
</head>
<body>
    <div class="temp_container">
        <div class="header">
            <span class="heading">Temperature Converter</span>
            <span class="icon"><i class="fas fa-temperature-high"></i></span>
        </div>
        <div class="text_symbol">
                 <span>&#8451 &#8457</span>
                 <span class="temp_icon"><i class="fas fa-cloud-sun-rain"></i></span>
        </div>
        <div class="input_Tempurature">
            <div class="celsius">
                <span class="text_celsius">Celsius &#8451</span>
                <input type="number" value="0" id="celsius">
            </div>
            <div class="fahrenheit">
                <span class="text_fahrenheit">Fahrenheit &#8457</span>
                <input type="number" value="32" id="fahrenheit">
            </div>
        </div>
    </div>


</body>
<script>
    var celsius =document.getElementById("celsius");
    var fahrenheit =document.getElementById("fahrenheit");

    celsius.addEventListener('input', function(){
        let cel = this.value;
        let fah = (cel * 9/5) + 32; //applying formula
        if(!Number.isInteger(fah)){
            fah = fah.toFixed(4);
        }
        fahrenheit.value = fah;
    });

    fahrenheit.addEventListener('input', function(){
        let fah = this.value;
        let cel = (fah - 32) * 5/9;
        if(!Number.isInteger(cel)){
            cel = cel.toFixed(4);
        }
        celsius.value = cel;
    });
</script>
</html>
