<script>
  import '$lib/Styles/Global.css'
  import'$lib/Styles/Forms.css';
</script>
  <div class="formcard-container">
    <div class="formcard">
      <h1>Iniciar Sesión</h1>
      <form>
        <label for="correo">
        <img src="/icons/mail.svg" alt="icono correo" class="icon" />Correo Electrónico
        </label>
        <input type="email" id="correo" name="correo" required>

        <label for="contrasena">
        <img src="/icons/lock.svg" alt="icono contraseña" class="icon" />Contraseña
        </label>
        <input type="password" id="contrasena" name="contrasena" required>

        <button class="entrar" type="submit">Entrar</button>
        <a href="/Login/Registrarse" class="crear">Crear cuenta</a>
      </form>
    </div>
  </div>