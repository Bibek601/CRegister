<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Login Page</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-image: url('SJLIC.jpeg'); /* Ensure this image is in the repository */
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
        }
        .login-container {
            background: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            text-align: center;
            width: 300px;
        }
        .login-container h2 {
            margin-bottom: 20px;
        }
        .input-group {
            margin-bottom: 15px;
            text-align: left;
        }
        .input-group label {
            display: block;
            margin-bottom: 5px;
        }
        .input-group input {
            width: 100%;
            padding: 8px;
            border: 1px solid #ccc;
            border-radius: 5px;
        }
        .login-btn {
            width: 100%;
            padding: 10px;
            background: #28a745;
            border: none;
            color: white;
            border-radius: 5px;
            cursor: pointer;
            font-size: 16px;
        }
        .login-btn:hover {
            background: #218838;
        }
        .logo {
            width: 200px;
            height: auto;
            margin-bottom: 20px;
        }
        .message {
            margin-top: 10px;
            font-size: 14px;
            font-weight: bold;
            color: red;
        }
    </style>
</head>
<body>
    <img src="SJLIC.png" alt="Logo" class="logo"> <!-- Ensure this image is in the repository -->
    <div class="login-container">
        <h2>Claim Register</h2>
        <h2>Login</h2>
        <form onsubmit="return validateLogin(event)">
            <div class="input-group">
                <label for="username">Username</label>
                <input type="text" id="username" name="username" required>
            </div>
            <div class="input-group">
                <label for="password">Password</label>
                <input type="password" id="password" name="password" required>
            </div>
            <button type="submit" class="login-btn">Login</button>
            <p id="message" class="message"></p>
        </form>
    </div>
    <script>
        function validateLogin(event) {
            event.preventDefault();
            const username = document.getElementById('username').value;
            const password = document.getElementById('password').value;
            const message = document.getElementById('message');

            if (username === 'Bibek' && password === 'Bibek') {
                message.style.color = 'green';
                message.textContent = 'Login successful. Please wait...';

                setTimeout(() => {
                    window.location.href = "main.html"; // Redirect to main page
                }, 1000);
            } else {
                message.style.color = 'red';
                message.textContent = 'Invalid username or password';
            }
        }
    </script>
</body>
</html>
