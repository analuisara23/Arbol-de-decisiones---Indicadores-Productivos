<style>
.flow-container { padding: 2rem 0; overflow-x: auto; }
.flow-stage { display: inline-block; vertical-align: top; margin: 0 2rem; min-width: 280px; }
.stage-title { font-size: 14px; font-weight: 500; color: var(--color-text-primary); margin-bottom: 1rem; text-align: center; }
.stage-box { background: var(--color-background-primary); border: 1px solid var(--color-border-tertiary); border-radius: var(--border-radius-lg); padding: 1.5rem; }
.stage-box.start { border: 2px solid var(--color-text-primary); background: var(--color-background-secondary); }
.stage-box.question { background: linear-gradient(135deg, var(--color-background-info) 0%, var(--color-background-primary) 100%); border-color: var(--color-border-info); }
.stage-box.mantener { border-left: 4px solid #0F6E56; background: linear-gradient(to bottom, #E1F5EE 0%, var(--color-background-primary) 20%); }
.stage-box.eliminar { border-left: 4px solid #A32D2D; background: linear-gradient(to bottom, #FCEBEB 0%, var(--color-background-primary) 20%); }
.stage-box.mover { border-left: 4px solid #BA7517; background: linear-gradient(to bottom, #FAEEDA 0%, var(--color-background-primary) 20%); }
.stage-box.nuevo { border-left: 4px solid #378ADD; background: linear-gradient(to bottom, #E6F1FB 0%, var(--color-background-primary) 20%); }
.big-number { font-size: 48px; font-weight: 500; line-height: 1; margin: 0 0 8px 0; text-align: center; }
.stage-label { font-size: 15px; font-weight: 500; text-align: center; margin: 0 0 12px 0; }
.stage-desc { font-size: 13px; color: var(--color-text-secondary); text-align: center; margin: 0 0 16px 0; line-height: 1.4; }
.indicator-list { margin: 1rem 0 0 0; max-height: 500px; overflow-y: auto; }
.indicator-item { padding: 8px 12px; margin: 6px 0; background: var(--color-background-secondary); border-radius: 6px; font-size: 12px; line-height: 1.5; cursor: pointer; transition: all 0.2s; }
.indicator-item:hover { background: var(--color-background-tertiary); transform: translateX(4px); }
.indicator-name { font-weight: 500; color: var(--color-text-primary); display: block; margin-bottom: 3px; }
.indicator-reason { color: var(--color-text-secondary); display: block; }
.redundant-tag { display: inline-block; padding: 2px 6px; background: #FCEBEB; color: #A32D2D; border-radius: 3px; font-size: 10px; font-weight: 500; margin-left: 4px; }
.arrow-connector { display: inline-block; font-size: 32px; color: var(--color-text-tertiary); margin: 0 -1rem; vertical-align: middle; }
.section-header { font-size: 13px; font-weight: 500; color: var(--color-text-primary); margin: 16px 0 8px 0; padding-top: 12px; border-top: 0.5px solid var(--color-border-tertiary); }
.section-header:first-child { border-top: none; padding-top: 0; }
.summary-box { margin: 2rem 0; padding: 1.5rem; background: var(--color-background-secondary); border-radius: var(--border-radius-lg); text-align: center; }
.equation { font-size: 32px; font-weight: 500; margin: 1rem 0; }
.equation .old { color: #A32D2D; }
.equation .new { color: #0F6E56; }
.speech-section { margin: 2rem 0; padding: 2rem; background: var(--color-background-primary); border: 1px solid var(--color-border-tertiary); border-radius: var(--border-radius-lg); }
.speech-title { font-size: 18px; font-weight: 500; margin: 0 0 1rem 0; color: var(--color-text-primary); }
.speech-step { margin: 1.5rem 0; padding-left: 1.5rem; border-left: 3px solid var(--color-border-info); }
.speech-step-title { font-size: 15px; font-weight: 500; color: var(--color-text-info); margin: 0 0 8px 0; }
.speech-text { font-size: 14px; color: var(--color-text-primary); line-height: 1.6; margin: 8px 0; }
.speech-text em { color: var(--color-text-secondary); font-style: italic; }
</style>

<div style="text-align: center; margin: 0 0 2rem 0;">
<div style="font-size: 28px; font-weight: 500; margin: 0 0 8px 0;">Árbol de Decisión Horizontal: 49 → 25 Indicadores</div>
<div style="font-size: 14px; color: var(--color-text-secondary);">Flujo completo de evaluación con todos los indicadores y redundancias identificadas</div>
</div>

<div class="flow-container">
<div style="white-space: nowrap; display: flex; align-items: center;">

<!-- INICIO -->
<div class="flow-stage">
<div class="stage-title">INICIO</div>
<div class="stage-box start">
<div class="big-number">49</div>
<div class="stage-label">Indicadores Actuales</div>
<div class="stage-desc">Modelo vigente de productividad</div>
</div>
</div>

<span class="arrow-connector">→</span>

<!-- PREGUNTA 1 -->
<div class="flow-stage">
<div class="stage-title">PREGUNTA 1</div>
<div class="stage-box question">
<div style="font-size: 16px; font-weight: 500; color: var(--color-text-info); margin-bottom: 8px;">¿Es estratégico para decisión ejecutiva?</div>
<div style="font-size: 12px; color: var(--color-text-secondary); line-height: 1.5;">¿Necesita la dirección este indicador para tomar decisiones de negocio?</div>
</div>
</div>

<span class="arrow-connector">→</span>

<!-- BIFURCACIÓN -->
<div class="flow-stage">
<div class="stage-title">RAMA A: ESTRATÉGICOS</div>
<div class="stage-box" style="border: 1px solid var(--color-border-info);">
<div class="big-number" style="color: #378ADD;">30</div>
<div class="stage-label">SÍ - Estratégico</div>
<div class="stage-desc">Críticos para dirección ejecutiva</div>
</div>

<div style="margin-top: 2rem;"></div>

<div class="stage-title">RAMA B: NO ESTRATÉGICOS</div>
<div class="stage-box" style="border: 1px solid var(--color-border-warning);">
<div class="big-number" style="color: #BA7517;">19</div>
<div class="stage-label">NO - No estratégico</div>
<div class="stage-desc">Operativos o de bajo valor</div>
</div>
</div>

<span class="arrow-connector">→</span>

<!-- PREGUNTA 2 PARA ESTRATÉGICOS -->
<div class="flow-stage">
<div class="stage-title">PREGUNTA 2 (Rama A)</div>
<div class="stage-box question">
<div style="font-size: 16px; font-weight: 500; color: var(--color-text-info); margin-bottom: 8px;">¿Ya existe otro que mida lo mismo?</div>
<div style="font-size: 12px; color: var(--color-text-secondary); line-height: 1.5;">¿Hay redundancia con otro indicador estratégico?</div>
</div>

<div style="margin-top: 2rem;"></div>

<div class="stage-title">PREGUNTA 3 (Rama B)</div>
<div class="stage-box question">
<div style="font-size: 16px; font-weight: 500; color: var(--color-text-info); margin-bottom: 8px;">¿Es útil para gerencias de área?</div>
<div style="font-size: 12px; color: var(--color-text-secondary); line-height: 1.5;">¿Lo usa algún gerente para gestión operativa?</div>
</div>
</div>

<span class="arrow-connector">→</span>

<!-- DESTINOS FINALES -->
<div class="flow-stage">
<div class="stage-title">DESTINO 1</div>
<div class="stage-box mantener">
<div class="big-number" style="color: #0F6E56;">21</div>
<div class="stage-label">✓ MANTENER</div>
<div class="stage-desc">Estratégico + único + esencial</div>

<div class="indicator-list">
<div class="section-header">Datos Absolutos Core (12)</div>
<div class="indicator-item">
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

<div style="margin-top: 2rem;"></div>

<div class="stage-title">DESTINO 2</div>
<div class="stage-box eliminar">
<div class="big-number" style="color: #A32D2D;">12</div>
<div class="stage-label">✗ ELIMINAR</div>
<div class="stage-desc">Redundantes o bajo valor</div>

<div class="indicator-list">
<div class="section-header">Redundancia de GastosOp (3)</div>
<div class="indicator-item">
<span class="indicator-name">1. GastosOp%Ventas <span class="redundant-tag">DUPLICA #16</span></span>
<span class="indicator-reason">Mide lo mismo que GastosOp%Ingresos - base diferente, insight idéntico</span>
</div>
<div class="indicator-item">
<span class="indicator-name">2. GastosOp%Contrato <span class="redundant-tag">DUPLICA #16</span></span>
<span class="indicator-reason">Otra forma de medir eficiencia operativa - no agrega perspectiva</span>
</div>
<div class="indicator-item">
<span class="indicator-name">3. GastosOp%Cartera <span class="redundant-tag">DUPLICA #16</span></span>
<span class="indicator-reason">Tercera variación del mismo concepto - multiplicidad sin valor</span>
</div>

<div class="section-header">Ratios de Bajo Valor (7)</div>
<div class="indicator-item">
<span class="indicator-name">4. Reserva%Contrato</span>
<span class="indicator-reason">Ya capturado en %90+ y Reserva Requerida - derivado obvio</span>
</div>
<div class="indicator-item">
<span class="indicator-name">5. Pagos%Contrato</span>
<span class="indicator-reason">Derivado sin valor diferencial - Pagos%Ventas es mejor</span>
</div>
<div class="indicator-item">
<span class="indicator-name">6. Ventas%Headcount <span class="redundant-tag">INFERIOR A #20</span></span>
<span class="indicator-reason">Ingresos/Headcount es mejor proxy de productividad financiera</span>
</div>
<div class="indicator-item">
<span class="indicator-name">7. Solicitudes%Headcount</span>
<span class="indicator-reason">No agrega valor vs Contratos/HC y Colocaciones/HC</span>
</div>
<div class="indicator-item">
<span class="indicator-name">8. Contrato 90+%Headcount</span>
<span class="indicator-reason">Ya capturado en %90+ - dividir por HC no agrega insight</span>
</div>
<div class="indicator-item">
<span class="indicator-name">9. PagosUnit%Headcount</span>
<span class="indicator-reason">Bajo valor estratégico - no usado en decisiones</span>
</div>
<div class="indicator-item">
<span class="indicator-name">10. CostoCrédito%Headcount</span>
<span class="indicator-reason">Bajo valor estratégico - división arbitraria</span>
</div>

<div class="section-header">Detalle Excesivo (2)</div>
<div class="indicator-item">
<span class="indicator-name">11. GastoPersonal%Ingresos <span class="redundant-tag">DENTRO DE #16</span></span>
<span class="indicator-reason">Ya incluido en GastosOp%Ingresos - sub-ratio innecesario</span>
</div>
<div class="indicator-item">
<span class="indicator-name">12. GastoPersonal%GastoOp</span>
<span class="indicator-reason">Composición interna - detalle no estratégico para dirección</span>
</div>
</div>
</div>

<div style="margin-top: 2rem;"></div>

<div class="stage-title">DESTINO 3</div>
<div class="stage-box mover">
<div class="big-number" style="color: #BA7517;">16</div>
<div class="stage-label">→ MOVER</div>
<div class="stage-desc">A reporting operativo (2do nivel)</div>

<div class="indicator-list">
<div class="section-header">Desglose Gastos por Área (7)</div>
<div class="indicator-item">
<span class="indicator-name">1. Créditos y Administración (gastos Lps)</span>
<span class="indicator-reason">Útil para gerente de área - demasiado granular para ejecutivo</span>
</div>
<div class="indicator-item">
<span class="indicator-name">2. Cobros (gastos Lps)</span>
<span class="indicator-reason">Control operativo de gerencia - no decisión estratégica</span>
</div>
<div class="indicator-item">
<span class="indicator-name">3. Comercial (gastos Lps)</span>
<span class="indicator-reason">Gestión de presupuesto de área - nivel táctico</span>
</div>
<div class="indicator-item">
<span class="indicator-name">4. Mercadeo (gastos Lps)</span>
<span class="indicator-reason">Control de inversión comercial - operativo</span>
</div>
<div class="indicator-item">
<span class="indicator-name">5. Oficina Central (gastos Lps)</span>
<span class="indicator-reason">Overhead detallado - no estratégico</span>
</div>
<div class="indicator-item">
<span class="indicator-name">6. Contact Center (gastos Lps)</span>
<span class="indicator-reason">Costo de servicio - gestión operativa</span>
</div>
<div class="indicator-item">
<span class="indicator-name">7. Gastos de Personal (valor absoluto)</span>
<span class="indicator-reason">Ya tenemos total y promedio - detalle innecesario ejecutivo</span>
</div>

<div class="section-header">Headcount por Área (5)</div>
<div class="indicator-item">
<span class="indicator-name">8. Créditos y Administración (HC)</span>
<span class="indicator-reason">Tamaño de equipo - gestión de gerente, no dirección</span>
</div>
<div class="indicator-item">
<span class="indicator-name">9. Cobros (HC)</span>
<span class="indicator-reason">Dotación operativa - nivel táctico</span>
</div>
<div class="indicator-item">
<span class="indicator-name">10. Comercial (HC)</span>
<span class="indicator-reason">Fuerza de ventas - control operativo</span>
</div>
<div class="indicator-item">
<span class="indicator-name">11. Mercadeo (HC)</span>
<span class="indicator-reason">Equipo de marketing - gestión de área</span>
</div>
<div class="indicator-item">
<span class="indicator-name">12. Oficina Central (HC)</span>
<span class="indicator-reason">Staff corporativo - detalle operativo</span>
</div>

<div class="section-header">Distribuciones % (4)</div>
<div class="indicator-item">
<span class="indicator-name">13. Créditos y Administración (%)</span>
<span class="indicator-reason">Composición porcentual - útil para gerente, no ejecutivo</span>
</div>
<div class="indicator-item">
<span class="indicator-name">14. Cobros (%)</span>
<span class="indicator-reason">Peso relativo - gestión operativa</span>
</div>
<div class="indicator-item">
<span class="indicator-name">15. Comercial (%)</span>
<span class="indicator-reason">Distribución interna - no estratégico</span>
</div>
<div class="indicator-item">
<span class="indicator-name">16. Mercadeo (%)</span>
<span class="indicator-reason">Participación en total - nivel táctico</span>
</div>
</div>
</div>

<div style="margin-top: 2rem;"></div>

<div class="stage-title">DESTINO 4</div>
<div class="stage-box nuevo">
<div class="big-number" style="color: #378ADD;">+4</div>
<div class="stage-label">★ AGREGAR</div>
<div class="stage-desc">Gaps críticos de rentabilidad</div>

<div class="indicator-list">
<div class="section-header">Indicadores Nuevos Críticos (4)</div>
<div class="indicator-item">
<span class="indicator-name">1. Margen Operativo por Contrato</span>
<span class="indicator-reason">CRÍTICO: (Ingresos - GastosOp - Costo Crédito) / Contratos. HOY NO SABEMOS si ganamos o perdemos dinero por contrato</span>
</div>
<div class="indicator-item">
<span class="indicator-name">2. CAC (Customer Acquisition Cost)</span>
<span class="indicator-reason">CRÍTICO: (Gastos Comercial + Mercadeo) / Contratos Colocados. Costo de adquisición NO MEDIDO hoy</span>
</div>
<div class="indicator-item">
<span class="indicator-name">3. CAC Payback</span>
<span class="indicator-reason">CRÍTICO: CAC / (Ingresos mensuales/Contrato). ¿En cuántos meses recuperamos la inversión comercial? NO EXISTE</span>
</div>
<div class="indicator-item">
<span class="indicator-name">4. Cobertura de Reserva</span>
<span class="indicator-reason">IMPORTANTE: Reserva Requerida / Cartera 90+. ¿La provisión cubre la mora real? Calidad de estimación de riesgo</span>
</div>
</div>
</div>

</div>

</div>
</div>

<div class="summary-box">
<div style="font-size: 18px; font-weight: 500; margin-bottom: 1rem;">Resultado Final del Análisis</div>
<div class="equation">
<span class="old">49</span>
<span style="color: var(--color-text-tertiary); margin: 0 12px;">→</span>
<span class="new">25</span>
</div>
<div style="font-size: 14px; color: var(--color-text-secondary); margin-top: 8px;">
21 mantener + 4 nuevos = 25 indicadores core para dashboard ejecutivo
</div>
<div style="display: inline-block; padding: 8px 20px; background: var(--color-background-success); color: var(--color-text-success); border-radius: 20px; font-size: 14px; font-weight: 500; margin-top: 16px;">
Reducción de complejidad: 49% sin pérdida de visibilidad
</div>
</div>

<div class="speech-section">
<div class="speech-title">🎤 Speech de Presentación al Subgerente (5 minutos)</div>

<div class="speech-step">
<div class="speech-step-title">1. APERTURA (30 segundos)</div>
<div class="speech-text">
"Buenos días. Hoy tenemos 49 indicadores de productividad. Les voy a mostrar cómo los evaluamos con criterio estratégico para llegar a 25 indicadores core que realmente necesitamos para tomar decisiones."
</div>
<div class="speech-text em">
[Proyectar el árbol horizontal]
</div>
</div>

<div class="speech-step">
<div class="speech-step-title">2. PRIMERA PREGUNTA (1 minuto)</div>
<div class="speech-text">
"Primera pregunta: <strong>¿Es estratégico para decisión ejecutiva?</strong>"
</div>
<div class="speech-text">
"30 indicadores sí lo son: cartera, contratos, ventas, ingresos, mora, ratios de eficiencia. Estos son los que ustedes necesitan ver cada mes para saber si el negocio va bien o mal."
</div>
<div class="speech-text">
"19 no son estratégicos. Por ejemplo: el headcount de Créditos y Administración, los gastos de Contact Center en lempiras. Estos son detalles que usa el gerente del área, no la dirección."
</div>
</div>

<div class="speech-step">
<div class="speech-step-title">3. SEGUNDA PREGUNTA - Redundancia (1 minuto)</div>
<div class="speech-text">
"De esos 30 estratégicos, preguntamos: <strong>¿Hay duplicados?</strong>"
</div>
<div class="speech-text">
"Encontramos que <strong>medimos gastos operativos de TRES formas distintas</strong>: GastosOp sobre Ventas, sobre Cartera, y sobre Ingresos. Las tres dicen exactamente lo mismo. Solo necesitamos UNA: GastosOp%Ingresos, que es el estándar bancario."
</div>
<div class="speech-text">
"Eso nos da 21 indicadores estratégicos únicos que SÍ mantenemos."
</div>
</div>

<div class="speech-step">
<div class="speech-step-title">4. TERCERA PREGUNTA - Utilidad operativa (45 segundos)</div>
<div class="speech-text">
"De los 19 no estratégicos, preguntamos: <strong>¿Sirven para las gerencias?</strong>"
</div>
<div class="speech-text">
"16 sí sirven: los gerentes de Comercial, Cobros, Créditos necesitan ver su headcount, sus gastos, sus porcentajes. Estos indicadores NO se eliminan, se MUEVEN a un reporte operativo de segundo nivel."
</div>
<div class="speech-text">
"Los otros 3 no sirven ni estratégico ni operativo: ratios como Solicitudes por Headcount que nadie usa. Esos sí se eliminan."
</div>
</div>

<div class="speech-step">
<div class="speech-step-title">5. LOS 4 NUEVOS - El punto crítico (1 minuto)</div>
<div class="speech-text">
"Y aquí está el problema más grave: <strong>hoy NO sabemos si ganamos o perdemos dinero por contrato.</strong>"
</div>
<div class="speech-text">
"Tenemos ingresos, gastos, y costo de crédito por separado, pero nunca los restamos para saber el margen real. Por eso agregamos 4 indicadores CRÍTICOS:"
</div>
<div class="speech-text">
"1. <strong>Margen Operativo por Contrato</strong>: ¿Cuánto ganamos realmente por cada contrato?<br>
2. <strong>CAC - Costo de Adquisición</strong>: ¿Cuánto gastamos en comercial y mercadeo para conseguir un cliente?<br>
3. <strong>CAC Payback</strong>: ¿En cuántos meses recuperamos esa inversión comercial?<br>
4. <strong>Cobertura de Reserva</strong>: ¿Nuestra provisión realmente cubre la mora que tenemos?"
</div>
<div class="speech-text">
"Sin estos 4, estamos volando a ciegas en rentabilidad."
</div>
</div>

<div class="speech-step">
<div class="speech-step-title">6. CIERRE (30 segundos)</div>
<div class="speech-text">
"En resumen: de 49 indicadores llegamos a 25."
</div>
<div class="speech-text">
"✓ Eliminamos 12 por redundancia masiva<br>
✓ Movemos 16 a reporting operativo donde sí sirven<br>
✓ Mantenemos 21 estratégicos únicos<br>
✓ Agregamos 4 críticos de rentabilidad"
</div>
<div class="speech-text">
"<strong>Resultado: 49% menos complejidad, cero pérdida de visibilidad, y por primera vez vamos a saber si cada contrato genera o destruye valor.</strong>"
</div>
<div class="speech-text em">
[Pausa para preguntas]
</div>
</div>

</div>

<script>
// Hacer scroll horizontal automático al centro al cargar
window.addEventListener('load', function() {
  const container = document.querySelector('.flow-container');
  if (container) {
    container.scrollLeft = (container.scrollWidth - container.clientWidth) / 2;
  }
});
</script>
