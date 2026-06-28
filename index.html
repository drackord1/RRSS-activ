<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Panel de control — Reactivación de redes</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@500;600;700&family=Inter:wght@400;500;600&family=JetBrains+Mono:wght@500;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg: #12161A;
    --surface: #1B2127;
    --surface-2: #222A32;
    --border: #2C3540;
    --text: #EDEFF2;
    --text-dim: #8C98A4;
    --amber: #E8A33D;
    --amber-dim: rgba(232,163,61,0.16);
    --green: #49B97C;
    --green-dim: rgba(73,185,124,0.16);
    --red: #D8654A;
    --red-dim: rgba(216,101,74,0.14);
    --gray-dim: rgba(140,152,164,0.14);
    --font-display: 'Space Grotesk', sans-serif;
    --font-body: 'Inter', sans-serif;
    --font-mono: 'JetBrains Mono', monospace;
  }
  *{ box-sizing: border-box; }
  body{
    margin:0;
    background: var(--bg);
    color: var(--text);
    font-family: var(--font-body);
    -webkit-font-smoothing: antialiased;
  }
  .wrap{
    max-width: 620px;
    margin: 0 auto;
    padding: 28px 18px 60px;
  }

  /* ---------- HEADER / GAUGE ---------- */
  .header{
    display:flex;
    align-items:center;
    justify-content:space-between;
    gap: 16px;
    margin-bottom: 28px;
  }
  .eyebrow{
    font-family: var(--font-mono);
    font-size: 11px;
    letter-spacing: 0.12em;
    color: var(--text-dim);
    text-transform: uppercase;
    margin: 0 0 6px 0;
  }
  .title{
    font-family: var(--font-display);
    font-weight: 600;
    font-size: 22px;
    margin: 0 0 4px 0;
    letter-spacing: -0.01em;
  }
  .subtitle{
    font-size: 13px;
    color: var(--text-dim);
    margin: 0;
  }
  .gauge{
    position: relative;
    width: 84px;
    height: 84px;
    flex-shrink: 0;
  }
  .gauge svg{ transform: rotate(-90deg); }
  .gauge-track{ fill: none; stroke: var(--surface-2); stroke-width: 8; }
  .gauge-fill{
    fill: none;
    stroke: var(--amber);
    stroke-width: 8;
    stroke-linecap: round;
    transition: stroke-dashoffset 0.5s ease, stroke 0.5s ease;
  }
  .gauge-readout{
    position: absolute;
    inset: 0;
    display:flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .gauge-pct{
    font-family: var(--font-mono);
    font-size: 17px;
    font-weight: 600;
  }
  .gauge-label{
    font-size: 9px;
    color: var(--text-dim);
    letter-spacing: 0.06em;
  }

  /* ---------- PHASE PANEL ---------- */
  .phase{
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 10px;
    margin-bottom: 16px;
    overflow: hidden;
    border-left: 3px solid var(--phase-color, var(--text-dim));
  }
  .phase-head{
    display:flex;
    align-items: baseline;
    justify-content: space-between;
    gap: 10px;
    padding: 14px 16px 10px;
  }
  .phase-name{
    font-family: var(--font-display);
    font-weight: 600;
    font-size: 14.5px;
    margin: 0;
  }
  .phase-name span{ color: var(--phase-color); }
  .phase-count{
    font-family: var(--font-mono);
    font-size: 12px;
    color: var(--text-dim);
    white-space: nowrap;
  }
  .phase-desc{
    font-size: 12px;
    color: var(--text-dim);
    margin: 0 16px 10px;
  }

  /* ---------- TASK ROW ---------- */
  .task{
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 10px 16px;
    border-top: 1px solid var(--border);
    cursor: pointer;
    user-select: none;
  }
  .task:hover{ background: var(--surface-2); }
  .light{
    flex-shrink: 0;
    width: 22px;
    height: 22px;
    border-radius: 50%;
    border: 2px solid var(--border);
    background: transparent;
    position: relative;
    transition: background 0.2s ease, border-color 0.2s ease, box-shadow 0.2s ease;
  }
  .light::after{
    content:"";
    position:absolute;
    inset:0;
    border-radius: 50%;
  }
  .task[data-state="0"] .light{ background: var(--gray-dim); border-color: var(--border); }
  .task[data-state="1"] .light{ background: var(--amber); border-color: var(--amber); box-shadow: 0 0 0 4px var(--amber-dim); }
  .task[data-state="2"] .light{ background: var(--green); border-color: var(--green); box-shadow: 0 0 0 4px var(--green-dim); }
  .task[data-state="2"] .light::after{
    content:"✓";
    position:absolute;
    inset:0;
    display:flex;
    align-items:center;
    justify-content:center;
    font-size: 13px;
    color: #0E1A14;
    font-weight: 700;
  }
  .task-text{
    flex: 1;
    font-size: 13.5px;
    line-height: 1.4;
  }
  .task[data-state="2"] .task-text{ color: var(--text-dim); text-decoration: line-through; text-decoration-color: var(--border); }
  .task-status{
    font-family: var(--font-mono);
    font-size: 10px;
    letter-spacing: 0.04em;
    color: var(--text-dim);
    white-space: nowrap;
    text-transform: uppercase;
  }
  .task[data-state="1"] .task-status{ color: var(--amber); }
  .task[data-state="2"] .task-status{ color: var(--green); }

  .light:focus-visible, .task:focus-visible{
    outline: 2px solid var(--amber);
    outline-offset: 2px;
  }

  .footer{
    text-align: center;
    font-size: 11.5px;
    color: var(--text-dim);
    margin-top: 22px;
  }
  .footer button{
    background: none;
    border: none;
    color: var(--text-dim);
    text-decoration: underline;
    font-size: 11.5px;
    cursor: pointer;
    font-family: var(--font-body);
    padding: 0;
  }
  .footer button:hover{ color: var(--red); }

  .loading{
    text-align:center;
    color: var(--text-dim);
    font-size: 13px;
    padding: 60px 0;
  }

  @media (prefers-reduced-motion: reduce){
    .gauge-fill{ transition: none; }
  }
</style>
</head>
<body>
  <div class="wrap">
    <div class="header">
      <div>
        <p class="eyebrow">Plan de comunicación · post-sismo</p>
        <h1 class="title">Reactivación de redes</h1>
        <p class="subtitle" id="counter-text">cargando…</p>
      </div>
      <div class="gauge">
        <svg width="84" height="84" viewBox="0 0 84 84">
          <circle class="gauge-track" cx="42" cy="42" r="36"></circle>
          <circle class="gauge-fill" id="gauge-fill" cx="42" cy="42" r="36"
            stroke-dasharray="226.2" stroke-dashoffset="226.2"></circle>
        </svg>
        <div class="gauge-readout">
          <div class="gauge-pct" id="gauge-pct">0%</div>
          <div class="gauge-label">AVANCE</div>
        </div>
      </div>
    </div>

    <div id="content">
      <div class="loading">Cargando tu progreso…</div>
    </div>

    <div class="footer">
      Tocá cada indicador para alternar: pendiente → en proceso → listo.<br>
      Tu avance se guarda automáticamente. <button id="reset-btn">Reiniciar checklist</button>
    </div>
  </div>

<script>
const PHASES = [
  {
    id: 'f0',
    name: 'Fase 0 — Pausa y respeto',
    color: '#D8654A',
    desc: 'Rescate activo. No se reactiva nada todavía.',
    tasks: [
      'Pausar el calendario de contenido habitual',
      'Publicar un único mensaje de solidaridad (sin logo protagónico, sin CTA)',
      'Cerrar o moderar los comentarios en todas las redes',
      'Evaluar una utilidad real y genuina del equipo (ej. chequeo vehicular post-sismo)',
      'Brief de sensibilidad al equipo (CM + diseñadores)',
      'Monitoreo activo de menciones y comentarios',
    ],
  },
  {
    id: 'f1',
    name: 'Fase 1 — Transición a la recuperación',
    color: '#E8A33D',
    desc: 'El rescate empieza a ceder. Contenido funcional, sin venta.',
    tasks: [
      'Publicar contenido funcional: cómo revisar tu auto después de un sismo',
      'Comunicar apoyo logístico real, si existe (sin estética de campaña)',
      'Compartir testimonios y agradecimientos a rescatistas',
      'Ajustar paleta visual y ritmo de publicación',
    ],
  },
  {
    id: 'f2',
    name: 'Fase 2 — Reactivación real',
    color: '#49B97C',
    desc: 'El país empieza a respirar. Vuelta gradual a lo comercial.',
    tasks: [
      'Mensaje de transparencia: "pausamos por respeto, gracias por entender"',
      'Retomar contenido de comunidad antes que de producto',
      'Reintroducir gradualmente el contenido comercial',
      'Mantener un tono ajustado (sin lujo ostentoso ni triunfalismo)',
      'Recuperar el calendario editorial habitual',
    ],
  },
];

const STORAGE_KEY = 'checklist-reactivacion-state';
let state = {};
let allTaskIds = [];

PHASES.forEach(phase => {
  phase.tasks.forEach((_, i) => allTaskIds.push(phase.id + '-' + i));
});

function buildUI(){
  const content = document.getElementById('content');
  content.innerHTML = '';
  PHASES.forEach(phase => {
    const panel = document.createElement('div');
    panel.className = 'phase';
    panel.style.setProperty('--phase-color', phase.color);

    const doneCount = phase.tasks.filter((_, i) => state[phase.id + '-' + i] === 2).length;

    panel.innerHTML = `
      <div class="phase-head">
        <h2 class="phase-name">${phase.name}</h2>
        <span class="phase-count">${doneCount}/${phase.tasks.length}</span>
      </div>
      <p class="phase-desc">${phase.desc}</p>
    `;

    phase.tasks.forEach((text, i) => {
      const id = phase.id + '-' + i;
      const st = state[id] || 0;
      const row = document.createElement('div');
      row.className = 'task';
      row.setAttribute('data-state', st);
      row.setAttribute('tabindex', '0');
      row.setAttribute('role', 'button');
      row.dataset.taskId = id;
      row.innerHTML = `
        <span class="light"></span>
        <span class="task-text">${text}</span>
        <span class="task-status">${labelFor(st)}</span>
      `;
      row.addEventListener('click', () => cycleTask(id));
      row.addEventListener('keydown', (e) => {
        if(e.key === 'Enter' || e.key === ' '){ e.preventDefault(); cycleTask(id); }
      });
      panel.appendChild(row);
    });

    content.appendChild(panel);
  });
}

function labelFor(st){
  return st === 2 ? 'Listo' : st === 1 ? 'En proceso' : 'Pendiente';
}

function cycleTask(id){
  const current = state[id] || 0;
  const next = (current + 1) % 3;
  state[id] = next;
  saveState();
  updateTaskRow(id, next);
  updateSummary();
}

function updateTaskRow(id, st){
  const row = document.querySelector(`[data-task-id="${id}"]`);
  if(!row) return;
  row.setAttribute('data-state', st);
  row.querySelector('.task-status').textContent = labelFor(st);
  const phaseId = id.split('-')[0];
  const phase = PHASES.find(p => p.id === phaseId);
  const doneCount = phase.tasks.filter((_, i) => state[phaseId + '-' + i] === 2).length;
  const countEl = row.closest('.phase').querySelector('.phase-count');
  countEl.textContent = `${doneCount}/${phase.tasks.length}`;
}

function updateSummary(){
  const total = allTaskIds.length;
  const weight = allTaskIds.reduce((sum, id) => {
    const st = state[id] || 0;
    return sum + (st === 2 ? 1 : st === 1 ? 0.5 : 0);
  }, 0);
  const pct = Math.round((weight / total) * 100);
  const doneCount = allTaskIds.filter(id => state[id] === 2).length;
  const inProgressCount = allTaskIds.filter(id => state[id] === 1).length;

  document.getElementById('gauge-pct').textContent = pct + '%';
  document.getElementById('counter-text').textContent =
    `${doneCount} de ${total} listas · ${inProgressCount} en proceso`;

  const circumference = 226.2;
  const offset = circumference - (pct / 100) * circumference;
  const fill = document.getElementById('gauge-fill');
  fill.setAttribute('stroke-dashoffset', offset);
  fill.style.stroke = pct === 100 ? '#49B97C' : '#E8A33D';
}

async function loadState(){
  try{
    const result = await window.storage.get(STORAGE_KEY, false);
    if(result && result.value){
      state = JSON.parse(result.value);
    }
  }catch(err){
    state = {};
  }
}

async function saveState(){
  try{
    await window.storage.set(STORAGE_KEY, JSON.stringify(state), false);
  }catch(err){
    console.error('No se pudo guardar el progreso', err);
  }
}

document.getElementById('reset-btn').addEventListener('click', async () => {
  if(!confirm('¿Reiniciar todo el checklist?')) return;
  state = {};
  await saveState();
  buildUI();
  updateSummary();
});

(async function init(){
  await loadState();
  buildUI();
  updateSummary();
})();
</script>
</body>
</html>
