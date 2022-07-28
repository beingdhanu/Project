<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device- width, initial-scale=1.0">
    <title>Document</title>
</head>

<body>
    <form onsubmit="return check()"> password : <br>
        <input type="password" id="password"><br>
        re-enter to verify: <p id="msg" style="color: red;"></p>
        <input type="password" id="password2">
        <p id="msg2" style="color: red;"></p> <br>
        <input type="submit">
    </form>
    <script>
        function check() {
            let pcheck = document.getElementById("password").value;
            let pcheck2 = document.getElementById("password2").value;
            if (pcheck == "") {
                document.getElementById("msg").innerHTML = "fill the password";
                return false;
            }
            if (pcheck.length < 8) {
                document.getElementById("msg").innerHTML = "charactetr must be greater than 8";
                return false;
            }
            if (pcheck != pcheck2) {
                document.getElementById("msg2").innerHTML = "both password does not match";
                return false;
            }
        }
    </script>
</body>

</html>
