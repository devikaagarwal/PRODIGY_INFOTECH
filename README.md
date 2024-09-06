<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive navigation menu</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
        }
        .navbar {
            position:fixed;
            top: 0;
            width: 100%;
            background-color: transparent;
            transition: background-color 0.3s;
            padding: 15px;
            box-shadow: none;
        }
        .navbar.scrolled {
            background-color: purple;
            box-shadow: 0 2px 5px aqua;
        }
        .navbar a {
            color: white;
            text-decoration: none;
            padding: 15px;
            transition: color 0.3s;
        }
        .navbar a:hover {
            color: #ff6347;
        }
        .content {
            padding-top: 70px;
            height: 2000px;
        }
    </style>
</head>
<body>

    <div class="navbar" id="navbar">
        <a href="#home">Home</a>
        <a href="#about">About</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
    </div>

    <div class="content">
        <h1>Welcome to Our Website</h1>
        <p>Scroll down to see the effect on the navigation menu.</p>
    </div>

    <script>
        window.onscroll = function() {
            var navbar = document.getElementById("navbar");
            if (document.body.scrollTop > 50 || document.documentElement.scrollTop > 50) {
                navbar.classList.add("scrolled");
            } else {
                navbar.classList.remove("scrolled");
            }
        };
    </script>

</body>
</html>
