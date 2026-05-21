<style>
.stage-container { max-width: 800px; margin: 0 auto 2rem auto; }
.stage-box { background: var(--color-background-primary); border: 1px solid var(--color-border-tertiary); border-radius: var(--border-radius-lg); padding: 1.5rem; }
.stage-box.start { border: 2px solid var(--color-text-primary); background: var(--color-background-secondary); }
.stage-box.question { background: linear-gradient(135deg, var(--color-background-info) 0%, var(--color-background-primary) 100%); border: 1px solid var(--color-border-info); }
.stage-box.mantener { border-left: 4px solid #0F6E56; }
.stage-box.eliminar { border-left: 4px solid #A32D2D; }
.stage-box.mover { border-left: 4px solid #BA7517; }
.stage-box.nuevo { border-left: 4px solid #378ADD; }
.big-number { font-size: 56px; font-weight: 500; line-height: 1; text-align: center; margin: 0 0 8px 0; }
.stage-title { font-size: 16px; font-weight: 500; text-align: center; margin: 0 0 8px 0; }
.stage-desc { font-size: 13px; color: var(--color-text-secondary); text-align: center; margin: 0; line-height: 1.5; }
.arrow-down { text-align: center; font-size: 32px; color: var(--color-text-tertiary); margin: 1.5rem 0; }
.split-container { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin: 2rem 0; }
.branch-box { background: var(--color-background-primary); border: 1px solid var(--color-border-tertiary); border-radius: var(--border-radius-md); padding: 1.25rem; text-align: center; }
.branch-number { font-size: 42px; font-weight: 500; line-height: 1; margin: 0 0 6px 0; }
.branch-label { font-size: 15px; font-weight: 500; margin: 0 0 6px 0; }
.branch-desc { font-size: 12px; color: var(--color-text-secondary); margin: 0; }
.indicator-list { margin: 1.5rem 0 0 0; }
.section-header { font-size: 14px; font-weight: 500; color: var(--color-text-primary); margin: 20px 0 12px 0; padding-top: 16px; border-top: 0.5px solid var(--color-border-tertiary); }
.section-header:first-child { border-top: none; padding-top: 0; margin-top: 0; }
.indicator-item { padding: 10px 12px; margin: 8px 0; background: var(--color-background-secondary); border-radius: 6px; font-size: 13px; line-height: 1.5; cursor: pointer; transition: all 0.2s; }
.indicator-item:hover { background: var(--color-background-tertiary); transform: translateX(4px); }
.indicator-name { font-weight: 500; color: var(--color-text-primary); display: block; margin-bottom: 4px; }
.indicator-reason { color: var(--color-text-secondary); display: block; font-size: 12px; }
.redundant-tag { display: inline-block; padding: 2px 8px; background: #FCEBEB; color: #A32D2D; border-radius: 3px; font-size: 10px; font-weight: 500; margin-left: 6px; }
.summary-final { margin: 3rem auto 0; max-width: 700px; padding: 2rem; background: var(--color-background-secondary); border-radius: var(--border-radius-lg); text-align: center; }
.equation { font-size: 36px; font-weight: 500; margin: 1.5rem 0; }
.equation .old { color: #A32D2D; }
.equation .new { color: #0F6E56; }
.impact-badge { display: inline-block; padding: 10px 24px; background: var(--color-background-success); color: var(--color-text-success); border-radius: 24px; font-size: 15px; font-weight: 500; margin-top: 16px; }
</style>

<div style="text-align: center; margin: 0 0 3rem 0;">
<div style="font-size: 32px; font-weight: 500; margin: 0 0 12px 0;">Árbol de Decisión: Evaluación de Indicadores</div>
<div style="font-size: 15px; color: var(--color-text-secondary);">Análisis completo de 49 indicadores con redundancias identificadas</div>
</div>

<!-- NIVEL 1: INICIO -->
<div class="stage-container">
<div class="stage-box start">
<div class="big-number">49</div>
<div class="stage-title">Indicadores Actuales</div>
<div class="stage-desc">Modelo vigente de productividad</div>
</div>
</div>

<div class="arrow-down">↓</div>

<!-- NIVEL 2: PREGUNTA 1 -->
<div class="stage-container">
<div class="stage-box question">
<div style="font-size: 18px; font-weight: 500; color: var(--color-text-info); margin-bottom: 10px;">¿Es estratégico para decisión ejecutiva?</div>
<div style="font-size: 13px; color: var(--color-text-secondary);">¿Necesita la dirección este indicador para tomar decisiones de negocio?</div>
</div>
</div>

<div class="arrow-down">↓</div>

<!-- NIVEL 3: BIFURCACIÓN -->
<div class="stage-container">
<div class="split-container">
<div class="branch-box" style="border: 2px solid var(--color-border-info);">
<div class="branch-number" style="color: #378ADD;">30</div>
<div class="branch-label">SÍ - Estratégico</div>
<div class="branch-desc">Crítico para dirección ejecutiva</div>
</div>
<div class="branch-box" style="border: 2px solid var(--color-border-warning);">
<div class="branch-number" style="color: #BA7517;">19</div>
<div class="branch-label">NO - No estratégico</div>
<div class="branch-desc">Operativo o bajo valor</div>
</div>
</div>
</div>

<div class="arrow-down">↓</div>

<!-- NIVEL 4: PREGUNTAS SECUNDARIAS -->
<div class="stage-container">
<div class="split-container">
<div class="stage-box question">
<div style="font-size: 16px; font-weight: 500; color: var(--color-text-info); margin-bottom: 8px;">¿Ya existe otro que mida lo mismo?</div>
<div style="font-size: 12px; color: var(--color-text-secondary);">(Para los 30 estratégicos)</div>
</div>
<div class="stage-box question">
<div style="font-size: 16px; font-weight: 500; color: var(--color-text-info); margin-bottom: 8px;">¿Es útil para gerencias de área?</div>
<div style="font-size: 12px; color: var(--color-text-secondary);">(Para los 19 no estratégicos)</div>
</div>
</div>
</div>

<div class="arrow-down">↓</div>

<!-- NIVEL 5: RESULTADOS FINALES -->
<div class="stage-container">

<!-- MANTENER -->
<div class="stage-box mantener" style="margin-bottom: 2rem;">
<div class="big-number" style="color: #0F6E56;">21</div>
<div class="stage-title">✓ MANTENER</div>
<div class="stage-desc">Estratégicos únicos y esenciales</div>

<div class="indicator-list">
<div class="section-header">Datos Absolutos Core (12)</div>
<div class="indicator-item" onclick="sendPrompt('Dame más detalle sobre por qué mantener Cartera')">
<span class="indicator-name">1. Cartera</span>
<span class="indicator-reason">Tamaño total del negocio - métrica fundamental de escala</span>
</div>
<div class="indicator-item">
<span class="indicator-name">2. Contratos Vigentes</span>
<span class="indicator-reason">Base de clientes activa - volumen operativo actual</span>
</div>
<div class="indicator-item">
<span class="indicator-name">3. Ventas</span>
<span class="indicator-reason">Generación de ingresos por desembolsos - top line</span>
</div>
<div class="indicator-item">
<span class="indicator-name">4. Pagos</span>
<span class="indicator-reason">Flujo de caja entrante - recuperación efectiva</span>
</div>
<div class="indicator-item">
<span class="indicator-name">5. Solicitudes</span>
<span class="indicator-reason">Pipeline comercial - demanda del mercado</span>
</div>
<div class="indicator-item">
<span class="indicator-name">6. Contratos Colocados</span>
<span class="indicator-reason">Producción comercial efectiva - conversión a negocio</span>
</div>
<div class="indicator-item">
<span class="indicator-name">7. 90+ (valor absoluto)</span>
<span class="indicator-reason">Cartera en mora absoluta - volumen del problema de cobranza</span>
</div>
<div class="indicator-item">
<span class="indicator-name">8. %90+ (porcentaje)</span>
<span class="indicator-reason">Mora estructural - calidad de cartera crítica para riesgo</span>
</div>
<div class="indicator-item">
<span class="indicator-name">9. Reserva Requerida</span>
<span class="indicator-reason">Provisión de riesgo - capital inmovilizado por mora</span>
</div>
<div class="indicator-item">
<span class="indicator-name">10. Costo Crédito</span>
<span class="indicator-reason">Costo de riesgo materializado - pérdidas por default</span>
</div>
<div class="indicator-item">
<span class="indicator-name">11. Ingresos</span>
<span class="indicator-reason">Resultado financiero total - bottom line operativo</span>
</div>
<div class="indicator-item">
<span class="indicator-name">12. Gastos Operativos (total)</span>
<span class="indicator-reason">Estructura de costos agregada - eficiencia operativa</span>
</div>

<div class="section-header">Headcount (1)</div>
<div class="indicator-item">
<span class="indicator-name">13. Headcount Total</span>
<span class="indicator-reason">Tamaño de organización - capacidad instalada</span>
</div>

<div class="section-header">Ratios Estratégicos (8)</div>
<div class="indicator-item">
<span class="indicator-name">14. Ticket Promedio</span>
<span class="indicator-reason">Monetización por contrato - tamaño promedio de negocio</span>
</div>
<div class="indicator-item">
<span class="indicator-name">15. Pagos%Ventas</span>
<span class="indicator-reason">Eficiencia de recuperación - qué % de lo vendido se cobra</span>
</div>
<div class="indicator-item">
<span class="indicator-name">16. GastosOp%Ingresos</span>
<span class="indicator-reason">Cost-to-income ratio estándar bancario - eficiencia operativa</span>
</div>
<div class="indicator-item">
<span class="indicator-name">17. Ingresos%Contrato</span>
<span class="indicator-reason">Rentabilidad unitaria - cuánto genera cada contrato</span>
</div>
<div class="indicator-item">
<span class="indicator-name">18. Gasto Personal Promedio</span>
<span class="indicator-reason">Costo laboral unitario - salario promedio organización</span>
</div>
<div class="indicator-item">
<span class="indicator-name">19. Contratos%Headcount</span>
<span class="indicator-reason">Productividad comercial - cartera por colaborador</span>
</div>
<div class="indicator-item">
<span class="indicator-name">20. Ingresos%Headcount</span>
<span class="indicator-reason">Productividad financiera - ingresos por colaborador</span>
</div>
<div class="indicator-item">
<span class="indicator-name">21. ColocaContratos%Headcount</span>
<span class="indicator-reason">Productividad de originación - nuevos contratos por persona</span>
</div>
</div>
</div>

<!-- ELIMINAR -->
<div class="stage-box eliminar" style="margin-bottom: 2rem;">
<div class="big-number" style="color: #A32D2D;">12</div>
<div class="stage-title">✗ ELIMINAR</div>
<div class="stage-desc">Redundantes o bajo valor estratégico</div>

<div class="indicator-list">
<div class="section-header">Redundancia de Gastos Operativos (3)</div>
<div class="indicator-item" onclick="sendPrompt('¿Por qué GastosOp%Ventas duplica GastosOp%Ingresos?')">
<span class="indicator-name">1. GastosOp%Ventas <span class="redundant-tag">DUPLICA #16</span></span>
<span class="indicator-reason">Mide lo mismo que GastosOp%Ingresos (#16) - base diferente, insight idéntico. Ventas e Ingresos son prácticamente iguales en este modelo.</span>
</div>
<div class="indicator-item">
<span class="indicator-name">2. GastosOp%Contrato <span class="redundant-tag">DUPLICA #16</span></span>
<span class="indicator-reason">Otra forma de medir eficiencia operativa (#16) - no agrega perspectiva estratégica diferencial</span>
</div>
<div class="indicator-item">
<span class="indicator-name">3. GastosOp%Cartera <span class="redundant-tag">DUPLICA #16</span></span>
<span class="indicator-reason">Tercera variación del mismo concepto (#16) - multiplicidad sin justificación de valor</span>
</div>

<div class="section-header">Ratios de Bajo Valor (7)</div>
<div class="indicator-item">
<span class="indicator-name">4. Reserva%Contrato</span>
<span class="indicator-reason">Ya capturado en %90+ (#8) y Reserva Requerida (#9) - derivado obvio sin valor agregado</span>
</div>
<div class="indicator-item">
<span class="indicator-name">5. Pagos%Contrato</span>
<span class="indicator-reason">Derivado sin valor diferencial - Pagos%Ventas (#15) es superior y más usado</span>
</div>
<div class="indicator-item">
<span class="indicator-name">6. Ventas%Headcount <span class="redundant-tag">INFERIOR A #20</span></span>
<span class="indicator-reason">Ingresos/Headcount (#20) es mejor proxy de productividad financiera real</span>
</div>
<div class="indicator-item">
<span class="indicator-name">7. Solicitudes%Headcount</span>
<span class="indicator-reason">No agrega valor vs Contratos/HC (#19) y Colocaciones/HC (#21) que miden conversión real</span>
</div>
<div class="indicator-item">
<span class="indicator-name">8. Contrato 90+%Headcount</span>
<span class="indicator-reason">Ya capturado en %90+ (#8) - dividir mora por HC no agrega insight estratégico</span>
</div>
<div class="indicator-item">
<span class="indicator-name">9. PagosUnit%Headcount</span>
<span class="indicator-reason">Bajo valor estratégico - no usado en decisiones de dirección</span>
</div>
<div class="indicator-item">
<span class="indicator-name">10. CostoCrédito%Headcount</span>
<span class="indicator-reason">Bajo valor estratégico - división arbitraria sin utilidad decisional</span>
</div>

<div class="section-header">Detalle Excesivo (2)</div>
<div class="indicator-item">
<span class="indicator-name">11. GastoPersonal%Ingresos <span class="redundant-tag">DENTRO DE #16</span></span>
<span class="indicator-reason">Ya incluido en GastosOp%Ingresos (#16) - sub-componente innecesario a nivel ejecutivo</span>
</div>
<div class="indicator-item">
<span class="indicator-name">12. GastoPersonal%GastoOp</span>
<span class="indicator-reason">Composición interna de costos - detalle no estratégico para dirección</span>
</div>
</div>
</div>

<!-- MOVER -->
<div class="stage-box mover" style="margin-bottom: 2rem;">
<div class="big-number" style="color: #BA7517;">16</div>
<div class="stage-title">→ MOVER A OPERATIVO</div>
<div class="stage-desc">Útiles para gerencias de área - Reporting de 2do nivel</div>

<div class="indicator-list">
<div class="section-header">Desglose Gastos por Área (7)</div>
<div class="indicator-item">
<span class="indicator-name">1. Créditos y Administración (gastos Lps)</span>
<span class="indicator-reason">Útil para gerente de área - demasiado granular para dashboard ejecutivo</span>
</div>
<div class="indicator-item">
<span class="indicator-name">2. Cobros (gastos Lps)</span>
<span class="indicator-reason">Control operativo de gerencia - no decisión estratégica de dirección</span>
</div>
<div class="indicator-item">
<span class="indicator-name">3. Comercial (gastos Lps)</span>
<span class="indicator-reason">Gestión de presupuesto de área - nivel táctico, no estratégico</span>
</div>
<div class="indicator-item">
<span class="indicator-name">4. Mercadeo (gastos Lps)</span>
<span class="indicator-reason">Control de inversión comercial - operativo para gerente de mercadeo</span>
</div>
<div class="indicator-item">
<span class="indicator-name">5. Oficina Central (gastos Lps)</span>
<span class="indicator-reason">Overhead detallado - no estratégico para dirección</span>
</div>
<div class="indicator-item">
<span class="indicator-name">6. Contact Center (gastos Lps)</span>
<span class="indicator-reason">Costo de servicio - gestión operativa de área</span>
</div>
<div class="indicator-item">
<span class="indicator-name">7. Gastos de Personal (valor absoluto)</span>
<span class="indicator-reason">Ya tenemos total (#12) y promedio (#18) - detalle innecesario nivel ejecutivo</span>
</div>

<div class="section-header">Headcount por Área (5)</div>
<div class="indicator-item">
<span class="indicator-name">8. Créditos y Administración (HC)</span>
<span class="indicator-reason">Tamaño de equipo - gestión de gerente, no dirección ejecutiva</span>
</div>
<div class="indicator-item">
<span class="indicator-name">9. Cobros (HC)</span>
<span class="indicator-reason">Dotación operativa - nivel táctico de área</span>
</div>
<div class="indicator-item">
<span class="indicator-name">10. Comercial (HC)</span>
<span class="indicator-reason">Fuerza de ventas - control operativo gerencial</span>
</div>
<div class="indicator-item">
<span class="indicator-name">11. Mercadeo (HC)</span>
<span class="indicator-reason">Equipo de marketing - gestión de área específica</span>
</div>
<div class="indicator-item">
<span class="indicator-name">12. Oficina Central (HC)</span>
<span class="indicator-reason">Staff corporativo - detalle operativo no ejecutivo</span>
</div>

<div class="section-header">Distribuciones Porcentuales (4)</div>
<div class="indicator-item">
<span class="indicator-name">13. Créditos y Administración (%)</span>
<span class="indicator-reason">Composición porcentual - útil para gerente, no para dirección ejecutiva</span>
</div>
<div class="indicator-item">
<span class="indicator-name">14. Cobros (%)</span>
<span class="indicator-reason">Peso relativo en total - gestión operativa de área</span>
</div>
<div class="indicator-item">
<span class="indicator-name">15. Comercial (%)</span>
<span class="indicator-reason">Distribución interna - no estratégico para dirección</span>
</div>
<div class="indicator-item">
<span class="indicator-name">16. Mercadeo (%)</span>
<span class="indicator-reason">Participación en total - nivel táctico de gerencia</span>
</div>
</div>
</div>

<!-- NUEVOS -->
<div class="stage-box nuevo">
<div class="big-number" style="color: #378ADD;">+4</div>
<div class="stage-title">★ AGREGAR NUEVOS</div>
<div class="stage-desc">Gaps críticos de rentabilidad - Hoy no existen</div>

<div class="indicator-list">
<div class="section-header">Indicadores Críticos Ausentes (4)</div>
<div class="indicator-item" onclick="sendPrompt('Explícame en detalle el Margen Operativo por Contrato')">
<span class="indicator-name">1. Margen Operativo por Contrato</span>
<span class="indicator-reason">CRÍTICO: (Ingresos - GastosOp - Costo Crédito) / Contratos. HOY NO SABEMOS si ganamos o perdemos dinero por cada contrato colocado</span>
</div>
<div class="indicator-item" onclick="sendPrompt('¿Cómo se calcula el CAC y por qué es crítico?')">
<span class="indicator-name">2. CAC (Customer Acquisition Cost)</span>
<span class="indicator-reason">CRÍTICO: (Gastos Comercial + Gastos Mercadeo) / Contratos Colocados. Costo de adquisición NO MEDIDO hoy - no sabemos cuánto invertimos por cliente</span>
</div>
<div class="indicator-item">
<span class="indicator-name">3. CAC Payback</span>
<span class="indicator-reason">CRÍTICO: CAC / (Ingresos mensuales por Contrato). ¿En cuántos meses recuperamos la inversión comercial? NO EXISTE - clave para ROI comercial</span>
</div>
<div class="indicator-item">
<span class="indicator-name">4. Cobertura de Reserva</span>
<span class="indicator-reason">IMPORTANTE: Reserva Requerida / Cartera 90+. ¿La provisión cubre la mora real? Calidad de estimación de riesgo no medida actualmente</span>
</div>
</div>
</div>

</div>

<!-- RESUMEN FINAL -->
<div class="summary-final">
<div style="font-size: 20px; font-weight: 500; margin-bottom: 1rem; color: var(--color-text-primary);">Resultado Final del Análisis</div>
<div class="equation">
<span class="old">49</span>
<span style="color: var(--color-text-tertiary); margin: 0 16px;">→</span>
<span class="new">25</span>
</div>
<div style="font-size: 15px; color: var(--color-text-secondary); margin: 1rem 0;">
21 mantener + 4 nuevos = 25 indicadores core
</div>
<div class="impact-badge">Reducción 49% sin pérdida de visibilidad</div>

<div style="margin-top: 2rem; padding-top: 2rem; border-top: 0.5px solid var(--color-border-tertiary); text-align: left;">
<div style="font-size: 14px; color: var(--color-text-primary); line-height: 1.7;">
<strong>Conclusión Ejecutiva:</strong> El modelo propuesto elimina redundancia masiva (3 formas de medir GastosOp → 1), separa indicadores estratégicos de operativos (16 a segundo nivel), y agrega capacidad crítica de gestión de rentabilidad unitaria (4 nuevos). Sin perder visibilidad, ganando claridad decisional y, por primera vez, sabiendo si cada contrato crea o destruye valor.
</div>
</div>
</div>
