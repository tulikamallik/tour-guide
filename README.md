<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>City Survival Kit</title>
    <style>
        /* General Styles */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            background-image: url(https://th.bing.com/th/id/R.99d1f4bc69e0003f82d9755c9806f330?rik=D4FQo4K5Gz6Z0w&pid=ImgRaw&r=0);
            height: 100%;
            background-size: cover;
            background-position: center;        
        }


        .content-container {
            text-align: center;
            padding: 50px;
        }

        
        .login-button {
            padding: 10px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        
        .register-button {
            padding: 10px 20px;
            background-color: #28a745; /* Green color for registration button */
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }

        
        .form-container {
            display: none;
            width: 300px;
            margin: auto;
            background-color: #fff;
            padding: 35px;
            border-radius: 5px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
        }


        .form-group {
            margin-bottom: 15px;
        }

        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }

        input[type="text"],
        input[type="password"] {
            width: 100%;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }

        button[type="submit"] {
            width: 100%;
            padding: 10px;
            background-color: #007bff;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div class="content-container" id="content-container"> 
        <h1>City Survival Kit</h1>
        <button class="login-button" id="login-button">Login</button>
        <button class="register-button" id="register-button">Register</button>
    </div>

    <div class="form-container" id="login-container">
        <h2>Login</h2>
        <form id="login-form">
            <div class="form-group">
                <label for="username">Username:</label>
                <input type="text" id="username" name="username" required>
            </div>
            <div class="form-group">
                <label for="password">Password:</label>
                <input type="password" id="password" name="password" required>
            </div>
            <button type="submit" class="login-button">Login</button>
        </form>
    </div>

    <div class="form-container" id="register-container">
        <h2>Register</h2>
        <form id="register-form">
            <div class="form-group">
                <label for="new-username">New Username:</label>
                <input type="text" id="new-username" name="new-username" required>
            </div>
            <div class="form-group">
                <label for="new-password">New Password:</label>
                <input type="password" id="new-password" name="new-password" required>
            </div>
            <button type="submit" class="register-button">Register</button>
        </form>
    </div>

    <script>
        const loginButton = document.getElementById("login-button");
        const registerButton = document.getElementById("register-button");
        const loginContainer = document.getElementById("login-container");
        const registerContainer = document.getElementById("register-container");

        loginButton.addEventListener("click", () => {
            loginContainer.style.display = "block";
            registerContainer.style.display = "none"; 
        });

        registerButton.addEventListener("click", () => {
            loginContainer.style.display = "none"; 
            registerContainer.style.display = "block";
        });

        const loginForm = document.getElementById("login-form");
loginForm.addEventListener("submit", function(event) {
    event.preventDefault();

    const username = document.getElementById("username").value;
    const password = document.getElementById("password").value;

    console.log(username, password); 

    if (username === "Admin" && password === "password") {
        window.location.href = "dashboard.html";
    } else {
        alert("Login failed. Please check your credentials.");
    }
});

        const registerForm = document.getElementById("register-form");
        registerForm.addEventListener("submit", function(event) {
            event.preventDefault();

            

            alert("Registration successful!");
            window.location.href = "dashboard.html";
        });
    </script>
</body>
</html>
