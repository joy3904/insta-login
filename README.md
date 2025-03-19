<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Instagram Login</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #fafafa;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
        }

        .login-container {
            background-color: #fff;
            border: 1px solid #dbdbdb;
            width: 350px;
            padding: 20px;
            text-align: center;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
        }

        .logo {
            font-family: 'Brush Script MT', cursive;
            font-size: 32px;
            margin-bottom: 20px;
        }

        input {
            width: 100%;
            padding: 10px;
            margin: 5px 0;
            border: 1px solid #dbdbdb;
            border-radius: 3px;
            font-size: 14px;
            background-color: #fafafa;
        }

        .login-btn {
            width: 100%;
            padding: 10px;
            background-color: #0095f6;
            border: none;
            border-radius: 3px;
            color: white;
            font-size: 14px;
            cursor: pointer;
            margin-top: 10px;
        }

        .login-btn:disabled {
            background-color: #b2dffc;
            cursor: not-allowed;
        }

        .separator {
            display: flex;
            align-items: center;
            margin: 15px 0;
        }

        .separator div {
            flex: 1;
            height: 1px;
            background-color: #dbdbdb;
        }

        .separator span {
            margin: 0 10px;
            font-size: 12px;
            color: #8e8e8e;
        }

        .facebook-login {
            background-color: #1877f2;
            color: white;
            font-size: 14px;
            padding: 10px;
            border-radius: 3px;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            margin-top: 10px;
        }

        .facebook-login img {
            width: 16px;
            margin-right: 8px;
        }

        .forgot-password {
            font-size: 12px;
            color: #385185;
            margin-top: 10px;
            text-decoration: none;
            display: block;
        }
    </style>
</head>
<body>

    <div class="login-container">
        <div class="logo">Instagram</div>
        
        <form id="login-form">
            <input type="text" id="username" placeholder="Phone number, username, or email" required>
            <input type="password" id="password" placeholder="Password" required>
            <button type="submit" id="login-btn" class="login-btn" disabled>Log In</button>
        </form>

        <div class="separator">
            <div></div>
            <span>OR</span>
            <div></div>
        </div>

        <div class="facebook-login">
            <img src="https://upload.wikimedia.org/wikipedia/commons/c/cd/Facebook_logo_%28square%29.png" alt="Facebook">
            Log in with Facebook
        </div>

        <a href="#" class="forgot-password">Forgot password?</a>
    </div>

    <script>
        const usernameInput = document.getElementById('username');
        const passwordInput = document.getElementById('password');
        const loginBtn = document.getElementById('login-btn');

        function validateForm() {
            if (usernameInput.value.trim() !== "" && passwordInput.value.trim() !== "") {
                loginBtn.disabled = false;
            } else {
                loginBtn.disabled = true;
            }
        }

        usernameInput.addEventListener('input', validateForm);
        passwordInput.addEventListener('input', validateForm);

        document.getElementById('login-form').addEventListener('submit', function(event) {
            event.preventDefault();
            alert(`Username: ${usernameInput.value}\nPassword: ${passwordInput.value}`);
        });
    </script>

</body>
</html>
