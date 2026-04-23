<script setup>
import ProjectStats from '../components/Dashboard/ProjectStats.vue'

// Función para exportar/imprimir
const exportarPDF = () => {
  window.print();
};
</script>

<template>
  <main class="dashboard-view">
    <header class="header-flex">
      <div>
        <h1>Dashboard de EstimaPro</h1>
        <p>Visualización en tiempo real del alcance y hitos SMART.</p>
      </div>
      <button @click="exportarPDF" class="btn-export">
        Exportar Estimación (PDF)
      </button>
    </header>
    
    <ProjectStats />

    <section class="progress-section">
      <h3>Progreso del MVP</h3>
      <div class="progress-bar">
        <div class="progress-fill" style="width: 78%;">78%</div>
      </div>
      <p class="caption">Incremento del 13% en este sprint (Exportación).</p>
    </section>

    <section class="wireframes-preview">
      <h3>Vista Previa de Wireframes</h3>
      <div class="placeholder-wireframe">
        [ Layout de Exportación Estructurado ]
      </div>
    </section>
  </main>
</template>

<style scoped>
.dashboard-view { padding: 40px; }
.header-flex { display: flex; justify-content: space-between; align-items: start; margin-bottom: 20px; }
.btn-export { 
  background-color: #42b983; 
  color: white; 
  border: none; 
  padding: 10px 20px; 
  border-radius: 5px; 
  cursor: pointer; 
  font-weight: bold;
}
.btn-export:hover { background-color: #33a06f; }
.progress-section { margin-top: 30px; }
.progress-bar { width: 100%; background: #eee; border-radius: 20px; overflow: hidden; margin: 10px 0; }
.progress-fill { background: #42b983; color: white; padding: 5px 15px; text-align: right; font-size: 0.8rem; }
.wireframes-preview { margin-top: 30px; }
.placeholder-wireframe { 
  height: 100px; 
  border: 2px dashed #ccc; 
  display: flex; 
  align-items: center; 
  justify-content: center; 
  color: #999;
}

/* Estilos para que la exportación se vea limpia al imprimir */
@media print {
  .btn-export { display: none; }
  .dashboard-view { padding: 0; }
}
</style>