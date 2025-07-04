<script>
  import '$lib/Styles/Global.css';
  import '$lib/Styles/Forms.css';
</script>

<div class="formcard-container">
  <div class="formcard">
    <h1>Iniciar Sesión</h1>
    <form>
      <label for="correo">
        <img src="/icons/mail.svg" alt="icono correo" class="icon" />
        Correo Electrónico
      </label>
      <input type="email" id="correo" name="correo" required />

      <label for="contrasena">
        <img src="/icons/lock.svg" alt="icono contraseña" class="icon" />
        Contraseña
      </label>
      <input type="password" id="contrasena" name="contrasena" required />

      <div class="usuario">
        
        <label for="rol">
          <img src="/icons/rol.svg" alt="icono contraseña" class="icon" />
          Rol
        </label>
        <select class="form-select" id="rol" name="rol" required>
          <option value="admin">Cliente</option>
          <option value="barbero">Barbero</option>
          <option value="cliente">Administrador</option>
        </select>
      </div>

      <button type="submit" class="entrar">Ingresar</button>

      <a href="/Login/Registrarse" class="crear">Crear cuenta</a>
    </form>
  </div>
</div>
