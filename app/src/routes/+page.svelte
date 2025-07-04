<script>
  import '$lib/Styles/Global.css';
  import '$lib/Styles/top.css';
  import '$lib/Styles/landing.css'
</script>

<!-- NAVBAR -->
<nav class="top">
  <div class="logo">
    <img src="/images/logo blanco.png" alt="Logo BarberSync" />
  </div>
  <div class="links">
    <a href="/Login" class="sesion">Iniciar Sesión</a>
    <a href="/Login/Registrarse" class="registrarse">Registrarse</a>
  </div>
</nav>

<!-- CARRUSEL -->
<div id="carruselServicios" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-inner">
    <div class="carousel-item active">
      <img src="https://www.somosmamas.com.ar/wp-content/uploads/2017/11/cortes-de-cabello-para-mujer-corto-10.jpg" class="d-block w-100" alt="Corte 1">
    </div>
    <div class="carousel-item">
      <img src="https://tse2.mm.bing.net/th/id/OIP.UP5wkc7S5yvPwGJ7rTWyUwHaFj?r=0&w=800&h=600&rs=1&pid=ImgDetMain" class="d-block w-100" alt="Afeitado">
    </div>
    <div class="carousel-item">
      <img src="https://www.carloscondepeluqueros.com/wp-content/uploads/2019/01/cabecera-barbero-profesional.jpg" class="d-block w-100" alt="Estilo">
    </div>
  </div>
<button class="carousel-control-prev" type="button" data-bs-target="#carruselServicios" data-bs-slide="prev" aria-label="Anterior">
  <span class="carousel-control-prev-icon" aria-hidden="true"></span>
</button>
<button class="carousel-control-next" type="button" data-bs-target="#carruselServicios" data-bs-slide="next" aria-label="Siguiente">
  <span class="carousel-control-next-icon" aria-hidden="true"></span>
</button>
</div>

<!-- INFO -->
<section class="container text-center py-5">
  <h2 class="mb-4">¿Qué es BarberSync?</h2>
  <p class="lead">Es una plataforma web donde las barberías pueden gestionar sus citas, sus barberos y recibir retroalimentación de sus clientes. Todo en un solo lugar, con un diseño moderno, seguro y fácil de usar.</p>
</section>

<!-- ACERCA -->
<section class="container py-5" id="acerca">
  <div class="row justify-content-center align-items-center g-4">
    <div class="col-md-6">
      <h3>Acerca de Nosotros</h3>
      <p>En BarberSync creemos en la transformación digital de las barberías locales. Nuestro objetivo es facilitar la administración de citas, mejorar la comunicación entre barberos y clientes, y ofrecer una experiencia de usuario profesional tanto para el cliente como para el administrador. Con nuestra plataforma, los clientes pueden agendar fácilmente sus servicios desde cualquier lugar, mientras que los barberos tienen acceso a una agenda organizada y herramientas que optimizan su tiempo.</p>
    </div>
    <div class="col-md-5">
      <img src="https://c8.alamy.com/compes/ptgxfd/guapo-seguros-maestros-mirando-a-la-camara-y-la-celebracion-de-unas-tijeras-en-la-mano-tres-peluqueros-profesionales-de-pie-cerca-de-peluqueria-sillas-y-posando-interior-de-barberia-ptgxfd.jpg" class="img-fluid rounded shadow" alt="Equipo BarberSync" style="max-height: 350px; object-fit: cover;">
    </div>
  </div>
</section>

<!-- BOTONES ROLES -->
<div class="d-flex justify-content-center my-4" id="botones-roles">
  <a href="admin.html" class="btn btn-primary mx-2">Administrador</a>
  <a href="cliente.html" class="btn btn-success mx-2">Cliente</a>
  <a href="barbero.html" class="btn btn-warning mx-2">Barbero</a>
</div>

<!-- MODAL -->
<div class="modal fade" id="modalLogin" tabindex="-1" aria-labelledby="modalLoginLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h5 class="modal-title" id="modalLoginLabel">Iniciar Sesión</h5>
        <button type="button" class="btn-close" data-bs-dismiss="modal"></button>
      </div>
      <div class="modal-body">
        <form>
          <div class="mb-3">
            <label for="correo" class="form-label">Correo electrónico</label>
            <input type="email" class="form-control" id="correo" placeholder="ejemplo@barbersync.com" required>
          </div>
          <div class="mb-3">
            <label for="password" class="form-label">Contraseña</label>
            <input type="password" class="form-control" id="password" placeholder="****" required>
          </div>
          <div class="mb-3">
            <label for="rol" class="form-label">Rol</label>
            <select class="form-select" id="rol">
              <option value="admin">Administrador</option>
              <option value="barbero">Barbero</option>
              <option value="cliente">Cliente</option>
            </select>
          </div>
          <button type="submit" class="btn btn-primary w-100">Ingresar</button>
        </form>
      </div>
    </div>
  </div>
</div>

<!-- FOOTER -->
<footer class="bg-dark text-white py-3">
  <div class="container text-center">
    <p>&copy; 2025 BarberSync. Todos los derechos reservados.</p>
  </div>
</footer>
