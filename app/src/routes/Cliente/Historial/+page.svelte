<script>
  import { onMount } from 'svelte';
  import '$lib/Styles/Global.css';
  import '$lib/Styles/nav.css';

  let citasPendientes = [];
  let citasRealizadas = [];

  // Simulación: Aquí luego se conecta a la API real
  onMount(async () => {
    try {
      const response = await fetch('/api/citas/cliente/1'); // Cambia el ID dinámicamente
      const data = await response.json();

      const ahora = new Date();

      citasPendientes = data.filter(cita => new Date(cita.fechaISO) >= ahora);
      citasRealizadas = data.filter(cita => new Date(cita.fechaISO) < ahora);
    } catch (error) {
      console.error('❌ Error al cargar citas:', error);
    }
  });

  function formatearFecha(fechaISO) {
    const fecha = new Date(fechaISO);
    return fecha.toLocaleDateString('es-MX');
  }

  function formatearHora(fechaISO) {
    const fecha = new Date(fechaISO);
    return fecha.toLocaleTimeString('es-MX', { hour: '2-digit', minute: '2-digit' });
  }
</script>

<!-- NAVBAR -->
<nav class="top">
  <div class="logo">
    <img src="/images/logo blanco.png" alt="Logo BarberSync" />
  </div>
</nav>

<h1 class="titulo-panel">
  <span style="color: white;">Historial de</span> Citas
</h1>

<section class="contenedor-historial">
  <div class="bloque-citas">
    <h2 class="titulo-seccion">📅 Pendientes</h2>
    {#if citasPendientes.length}
      {#each citasPendientes as cita}
        <div class="card-cita">
          <h3>{cita.servicio.nombre}</h3>
          <p><strong>Barbero:</strong> {cita.barbero.nombre}</p>
          <p><strong>Fecha:</strong> {formatearFecha(cita.fechaISO)}</p>
          <p><strong>Hora:</strong> {formatearHora(cita.fechaISO)}</p>
        </div>
      {/each}
    {:else}
      <p>No tienes citas pendientes.</p>
    {/if}
  </div>

  <div class="bloque-citas">
    <h2 class="titulo-seccion">✅ Realizadas</h2>
    {#if citasRealizadas.length}
      {#each citasRealizadas as cita}
        <div class="card-cita realizada">
          <h3>{cita.servicio.nombre}</h3>
          <p><strong>Barbero:</strong> {cita.barbero.nombre}</p>
          <p><strong>Fecha:</strong> {formatearFecha(cita.fechaISO)}</p>
          <p><strong>Hora:</strong> {formatearHora(cita.fechaISO)}</p>
        </div>
      {/each}
    {:else}
      <p>No tienes citas realizadas.</p>
    {/if}
  </div>
</section>

<style>
  .contenedor-historial {
    max-width: 900px;
    margin: auto;
    padding: 2rem;
    color: white;
    display: flex;
    flex-direction: column;
    gap: 3rem;
  }

  .bloque-citas {
    background-color: #2f2f2f;
    padding: 2rem;
    border-radius: 16px;
    box-shadow: 0 0 15px rgba(0,0,0,0.2);
  }

  .titulo-seccion {
    margin-bottom: 1rem;
    color: #C0A080;
  }

  .card-cita {
    background-color: #3a3a3a;
    border-left: 6px solid #C0A080;
    padding: 1rem;
    margin-bottom: 1rem;
    border-radius: 10px;
  }

  .card-cita.realizada {
    border-left: 6px solid #888;
    opacity: 0.8;
  }

  .card-cita h3 {
    margin: 0 0 0.5rem;
    color: #C0A080;
  }
</style>
