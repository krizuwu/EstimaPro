<script setup>
import ProjectStats from '../components/Dashboard/ProjectStats.vue'
</script>

<template>
  <main class="dashboard-view">
    <h1>Dashboard de EstimaPro</h1>
    <p>Visualización en tiempo real del alcance y hitos SMART[cite: 58].</p>
    
    <ProjectStats />

    <section class="progress-section">
      <h3>Progreso del MVP</h3>
      <div class="progress-bar">
        <div class="progress-fill" style="width: 65%;">65%</div>
      </div>
      <p class="caption">Basado en 45 Story Points totales[cite: 16].</p>
    </section>
  </main>
</template>

<style scoped>
.dashboard-view { padding: 40px; }
.progress-section { margin-top: 30px; }
.progress-bar { width: 100%; background: #eee; border-radius: 20px; overflow: hidden; margin: 10px 0; }
.progress-fill { background: #42b983; color: white; padding: 5px 15px; text-align: right; font-size: 0.8rem; }
.caption { font-size: 0.8rem; color: #888; }
</style>