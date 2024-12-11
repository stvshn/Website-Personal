<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
	<link rel="stylesheet" href="wall.css">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MASUKAN PASSWORD</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            background-color: #f4f4f4;
        }
        .login-container {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            width: 300px;
        }
        .error {
            color: red;
            font-size: 14px;
            margin-top: 10px;
        }
        .button {
            padding: 10px 20px;
            background-color: #007BFF;
            color: white;
            border: none;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
        }
        .button:hover {
            background-color: #0056b3;
        }
        .warning {
            display: none;
            margin-top: 10px;
            padding: 10px;
            background-color: #ff4d4d;
            color: white;
            border-radius: 4px;
            text-align: center;
        }
    </style>
</head>
<body>
    <div class="login-container">
        <h2>Login</h2>
        <form id="loginForm">
            <label for="password">Password:</label>
            <input type="password" id="password" name="password" required>
            <center><button type="submit">SUBMIT</button></center>
        </form>
        <p id="errorMessage" class="error" style="display: none;">Password Salah! Masukan Yang Benar!</p>

    <script>
        // Password yang benar
        const correctPassword = "12345";

        // Ambil elemen-elemen form dan pesan error
        const form = document.getElementById("loginForm");
        const passwordInput = document.getElementById("password");
        const errorMessage = document.getElementById("errorMessage");

        // Event listener untuk form
        form.addEventListener("submit", function(event) {
            event.preventDefault(); // Mencegah form submit secara default

            if (passwordInput.value === correctPassword) {
                console.log("Login Berhasil!");
				window.location.href = "profile.html";
                errorMessage.style.display = "none"; // Sembunyikan pesan error
            } else {
                errorMessage.style.display = "block"; // Tampilkan pesan error
            }
        });
    </script>
</body>
</html>
