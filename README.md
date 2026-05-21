<style>
body { margin: 0; padding: 1rem 0; }
.tree-container { max-width: 100%; margin: 0 auto; }
.level { margin: 2rem 0; }
.level-title { text-align: center; font-size: 14px; font-weight: 500; color: var(--color-text-secondary); margin-bottom: 1rem; }
.node-box { background: var(--color-background-primary); border: 1px solid var(--color-border-tertiary); border-radius: var(--border-radius-lg); padding: 1.5rem; margin: 0 auto; max-width: 560px; text-align: center; position: relative; }
.node-box.start { border: 2px solid var(--color-text-primary); background: var(--color-background-secondary); }
.node-number { font-size: 48px; font-weight: 500; line-height: 1; margin: 0 0 8px 0; color: var(--color-text-primary); }
.node-label { font-size: 16px; font-weight: 500; color: var(--color-text-primary); margin: 0; }
.node-sublabel { font-size: 13px; color: var(--color-text-secondary); margin: 8px 0 0 0; }
.question-box { background: linear-gradient(135deg, var(--color-background-info) 0%, var(--color-background-primary) 100%); border: 1px solid var(--color-border-info); border-radius: var(--border-radius-lg); padding: 1.25rem; margin: 0 auto; max-width: 480px; text-align: center; }
.question-text { font-size: 15px; font-weight: 500; color: var(--color-text-info); margin: 0; }
.branches { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 16px; margin: 2rem 0; max-width: 900px; margin-left: auto; margin-right: auto; }
.branch-node { background: var(--color-background-primary); border-radius: var(--border-radius-md); padding: 1rem; border: 1px solid var(--color-border-tertiary); cursor: pointer; transition: all 0.2s; }
.branch-node:hover { transform: translateY(-4px); border-color: var(--color-border-secondary); box-shadow: 0 4px 12px rgba(0,0,0,0.08); }
.branch-node.mantener { border-left: 4px solid #0F6E56; background: linear-gradient(to right, #E1F5EE 0%, var(--color-background-primary) 30%); }
.branch-node.eliminar { border-left: 4px solid #A32D2D; background: linear-gradient(to right, #FCEBEB 0%, var(--color-background-primary) 30%); }
.branch-node.mover { border-left: 4px solid #BA7517; background: linear-gradient(to right, #FAEEDA 0%, var(--color-background-primary) 30%); }
.branch-node.nuevo { border-left: 4px solid #378ADD; background: linear-gradient(to right, #E6F1FB 0%, var(--color-background-primary) 30%); }
.branch-count { font-size: 32px; font-weight: 500; line-height: 1; margin: 0 0 4px 0; }
.branch-label { font-size: 14px; font-weight: 500; margin: 0 0 6px 0; }
.branch-desc { font-size: 12px; color: var(--color-text-secondary); margin: 0; line-height: 1.4; }
.arrow-down { text-align: center; font-size: 24px; color: var(--color-text-tertiary); margin: 1rem 0; }
.final-summary { margin: 3rem auto 0; max-width: 640px; padding: 2rem; background: var(--color-background-secondary); border-radius: var(--border-radius-lg); text-align: center; }
.final-equation { font-size: 28px; font-weight: 500; margin: 1.5rem 0; color: var(--color-text-primary); }
.final-equation .old { color: #A32D2D; }
.final-equation .new { color: #0F6E56; }
.final-equation .arrow { color: var(--color-text-tertiary); margin: 0 12px; }
.impact-badge { display: inline-block; padding: 8px 20px; background: var(--color-background-success); color: var(--color-text-success); border-radius: 20px; font-size: 14px; font-weight: 500; margin-top: 12px; }
.examples-toggle { margin: 1.5rem 0; text-align: center; }
.examples-btn { padding: 8px 24px; background: var(--color-background-primary); border: 1px solid var(--color-border-secondary); border-radius: 20px; cursor: pointer; font-size: 13px; transition: all 0.2s; }
.examples-btn:hover { background: var(--color-background-secondary); }
.examples-list { display: none; margin-top: 1rem; padding: 1rem; background: var(--color-background-primary); border-radius: var(--border-radius-md); text-align: left; }
.examples-list.show { display: block; }
.example-item { padding: 8px 0; border-bottom: 0.5px solid var(--color-border-tertiary); font-size: 13px; }
.example-item:last-child { border-bottom: none; }
.example-name { font-weight: 500; color: var(--color-text-primary); }
.example-reason { color: var(--color-text-secondary); margin-left: 8px; }
</style>

<div class="tree-container">

<div class="level">
<div class="node-box start">
<div class="node-number">83</div>
<div class="node-label">Indicadores Actuales</div>
<div class="node-sublabel">Modelo de productividad vigente</div>
</div>
</div>

<div class="arrow-down">↓</div>

<div class="level">
<div class="level-title">Primera Pregunta</div>
<div class="question-box">
<div class="question-text">¿Es estratégico para decisión ejecutiva?</div>
</div>
</div>

<div class="arrow-down">↓</div>

<div class="level">
<div class="branches">
<div class="branch-node" style="border-left: 4px solid #378ADD;">
<div class="branch-count" style="color: #378ADD;">30</div>
<div class="branch-label">SÍ - Estratégico</div>
<div class="branch-desc">Crítico para dirección ejecutiva</div>
<div class="examples-toggle">
<button class="examples-btn" onclick="toggleExamples('estrategico')">Ver ejemplos ↓</button>
<div id="ejemplos-estrategico" class="examples-list">
<div class="example-item"><span class="example-name">Cartera total</span><span class="example-reason">- Tamaño del negocio</span></div>
<div class="example-item"><span class="example-name">%90+ (mora)</span><span class="example-reason">- Riesgo crítico</span></div>
<div class="example-item"><span class="example-name">Gastos Op % Ingresos</span><span class="example-reason">- Cost-to-income</span></div>
<div class="example-item"><span class="example-name">Contratos por HC</span><span class="example-reason">- Productividad</span></div>
</div>
</div>
</div>

<div class="branch-node" style="border-left: 4px solid #BA7517;">
<div class="branch-count" style="color: #BA7517;">53</div>
<div class="branch-label">NO - No estratégico</div>
<div class="branch-desc">Operativo o redundante</div>
<div class="examples-toggle">
<button class="examples-btn" onclick="toggleExamples('noestrategico')">Ver ejemplos ↓</button>
<div id="ejemplos-noestrategico" class="examples-list">
<div class="example-item"><span class="example-name">% HC Créditos</span><span class="example-reason">- Detalle operativo</span></div>
<div class="example-item"><span class="example-name">Gastos Op % Ventas</span><span class="example-reason">- Redundante</span></div>
<div class="example-item"><span class="example-name">Pagos por HC</span><span class="example-reason">- Bajo valor</span></div>
</div>
</div>
</div>
</div>
</div>

<div class="arrow-down">↓</div>

<div class="level">
<div class="level-title">Segunda Pregunta (Solo para estratégicos)</div>
<div class="question-box">
<div class="question-text">¿Ya existe otro indicador que mida lo mismo?</div>
</div>
</div>

<div class="arrow-down">↓</div>

<div class="level">
<div class="branches">
<div class="branch-node mantener" onclick="sendPrompt('Dame más detalle sobre los 26 indicadores que se mantienen')">
<div class="branch-count" style="color: #0F6E56;">26</div>
<div class="branch-label">✓ MANTENER</div>
<div class="branch-desc">Estratégico + No redundante</div>
</div>

<div class="branch-node eliminar" onclick="sendPrompt('¿Cuáles son los indicadores redundantes que se eliminan?')">
<div class="branch-count" style="color: #A32D2D;">4</div>
<div class="branch-label">✗ ELIMINAR</div>
<div class="branch-desc">Estratégico pero redundante</div>
<div class="examples-toggle">
<button class="examples-btn" onclick="toggleExamples('redundantes')">Ver ejemplos ↓</button>
<div id="ejemplos-redundantes" class="examples-list">
<div class="example-item"><span class="example-name">Gastos Op % Ventas</span><span class="example-reason">- Ya existe GastosOp%Ingresos</span></div>
<div class="example-item"><span class="example-name">Gastos Op % Cartera</span><span class="example-reason">- Mismo concepto, otra base</span></div>
<div class="example-item"><span class="example-name">Gastos Op % Contrato</span><span class="example-reason">- Sin valor diferencial</span></div>
</div>
</div>
</div>
</div>
</div>

<div class="arrow-down">↓</div>

<div class="level">
<div class="level-title">Tercera Pregunta (Para no estratégicos)</div>
<div class="question-box">
<div class="question-text">¿Es útil para gerencias de área?</div>
</div>
</div>

<div class="arrow-down">↓</div>

<div class="level">
<div class="branches">
<div class="branch-node mover" onclick="sendPrompt('¿Qué indicadores se mueven a reporting operativo?')">
<div class="branch-count" style="color: #BA7517;">~15</div>
<div class="branch-label">→ MOVER</div>
<div class="branch-desc">A reporting operativo (2do nivel)</div>
<div class="examples-toggle">
<button class="examples-btn" onclick="toggleExamples('mover')">Ver ejemplos ↓</button>
<div id="ejemplos-mover" class="examples-list">
<div class="example-item"><span class="example-name">Distribución HC por área</span><span class="example-reason">- Útil para gerente área</span></div>
<div class="example-item"><span class="example-name">Gastos detallados por centro</span><span class="example-reason">- Gestión operativa</span></div>
<div class="example-item"><span class="example-name">HC por departamento</span><span class="example-reason">- No es nivel ejecutivo</span></div>
</div>
</div>
</div>

<div class="branch-node eliminar" onclick="sendPrompt('¿Qué indicadores se eliminan por bajo valor?')">
<div class="branch-count" style="color: #A32D2D;">~38</div>
<div class="branch-label">✗ ELIMINAR</div>
<div class="branch-desc">Sin utilidad ni estratégica ni operativa</div>
<div class="examples-toggle">
<button class="examples-btn" onclick="toggleExamples('bajovalor')">Ver ejemplos ↓</button>
<div id="ejemplos-bajovalor" class="examples-list">
<div class="example-item"><span class="example-name">Ventas por HC</span><span class="example-reason">- Ingresos/HC es mejor</span></div>
<div class="example-item"><span class="example-name">Solicitudes por HC</span><span class="example-reason">- No agrega vs Contratos/HC</span></div>
<div class="example-item"><span class="example-name">Ratios derivados múltiples</span><span class="example-reason">- Complejidad sin valor</span></div>
</div>
</div>
</div>
</div>
</div>

<div class="arrow-down">↓</div>

<div class="level">
<div class="level-title">Adición Crítica</div>
<div class="branch-node nuevo" style="max-width: 560px; margin: 0 auto;" onclick="sendPrompt('Explícame los 4 nuevos indicadores de rentabilidad')">
<div class="branch-count" style="color: #378ADD;">+4</div>
<div class="branch-label">★ AGREGAR NUEVOS</div>
<div class="branch-desc">Gaps críticos en rentabilidad unitaria</div>
<div class="examples-toggle">
<button class="examples-btn" onclick="toggleExamples('nuevos')">Ver detalles ↓</button>
<div id="ejemplos-nuevos" class="examples-list">
<div class="example-item"><span class="example-name">Margen Operativo / Contrato</span><span class="example-reason">- Rentabilidad unitaria</span></div>
<div class="example-item"><span class="example-name">CAC</span><span class="example-reason">- Costo de adquisición</span></div>
<div class="example-item"><span class="example-name">CAC Payback</span><span class="example-reason">- ROI comercial</span></div>
<div class="example-item"><span class="example-name">Cobertura Reserva</span><span class="example-reason">- Calidad de provisiones</span></div>
</div>
</div>
</div>
</div>

<div class="final-summary">
<div style="font-size: 16px; font-weight: 500; margin-bottom: 1rem; color: var(--color-text-primary);">Resultado Final</div>
<div class="final-equation">
<span class="old">83</span>
<span class="arrow">→</span>
<span class="new">30</span>
</div>
<div style="font-size: 14px; color: var(--color-text-secondary); margin-top: 8px;">
26 mantener + 4 nuevos = 30 indicadores core
</div>
<div class="impact-badge">Reducción de complejidad: 65%</div>

<div style="margin-top: 2rem; padding-top: 2rem; border-top: 0.5px solid var(--color-border-tertiary);">
<div style="font-size: 13px; color: var(--color-text-secondary); line-height: 1.6;">
<strong style="color: var(--color-text-primary);">Conclusión Ejecutiva:</strong> El modelo propuesto elimina redundancia masiva (42 indicadores duplicados o de bajo valor), separa indicadores estratégicos de operativos (15 a segundo nivel), y agrega capacidad crítica de gestión de rentabilidad (4 nuevos). Sin perder visibilidad, ganando claridad decisional.
</div>
</div>
</div>

</div>

<script>
function toggleExamples(id) {
  const elem = document.getElementById('ejemplos-' + id);
  const allExamples = document.querySelectorAll('.examples-list');
  const wasVisible = elem.classList.contains('show');
  
  allExamples.forEach(e => e.classList.remove('show'));
  
  if (!wasVisible) {
    elem.classList.add('show');
  }
  
  event.target.textContent = elem.classList.contains('show') ? 'Ocultar ejemplos ↑' : 'Ver ejemplos ↓';
}
</script>
