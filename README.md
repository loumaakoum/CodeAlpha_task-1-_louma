# CodeAlpha_task-1-_louma
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        input
        {
            font-family: algerian;
            font-size: 22;
            background-color: aqua;
            color: blue;
        }

        #fullInfo
        {
            font-family: monotype corsiva;
            font-size: 26;
        } 
    </style>
    <script>
        function show()
        {
            var name = prompt ("Please enter your name");
            var niveau;
            do
            {
                var gender = prompt ("Enter your gender (male or female)");
            }while (gender != "male" && gender !="female");
            var genkind;
            if (gender == "male")
            {
                genkind == "Mr. ";
            }
            else
            {
                genkind = "Miss ";

            }
            var yob = prompt ("Enter your year of birth");
            var age = calculateAge(yob);
            if(age<11)
            {
                niveau = "child"
            }
            else if (age<18)
            {
                niveau = "Teenager";
            }
            else if(age<60)
            {
                niveau = "Adult";
            }
            else
            {
                niveau = "age";
            }
            var info = "Hello " + genkind + name.toUpperCase() + " (" + age + "years old). you  are a " + niveau;
            document.getElementById("fullInfo").innerHTML = info;
            
        }
        function calculateAge(y)
        {
            var now = new Date();
            var year = now.getFullYear();
            var age = year - y;
            return age;
        }

    </script>
</head>
<body>

    <center>
        <input type="button" value="Enter your Info." onclick="show()">
        <div id="fullInfo"></div>
    </center>
</body>
</html>
