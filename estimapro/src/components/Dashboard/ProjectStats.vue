<template>
  <div class="stats-container">
    <h3>Resumen de Estimación - Sprint 4</h3>
    <div class="grid-stats">
      <div class="stat-card">
        <span>Frontend</span>
        <strong>3 historias</strong>
      </div>
      <div class="stat-card">
        <span>Backend</span>
        <strong>4 historias</strong>
      </div>
      <div class="stat-card">
        <span>Base de Datos</span>
        <strong>3 historias</strong>
      </div>
    </div>
  </div>
</template>

<style scoped>
.stats-container { padding: 20px; background: #f9f9f9; border-radius: 8px; }
.grid-stats { display: grid; grid-template-columns: repeat(3, 1fr); gap: 15px; margin-top: 10px; }
.stat-card { padding: 15px; background: white; border: 1px solid #ddd; text-align: center; border-radius: 5px; }
.stat-card span { display: block; font-size: 0.9rem; color: #666; }
.stat-card strong { font-size: 1.5rem; color: #42b983; }
</style>