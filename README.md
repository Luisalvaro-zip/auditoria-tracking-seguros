# Auditoría de Medición Digital — Cotizador SOAT Pacífico Seguros

## ¿De qué trata este proyecto?

Auditoría técnica e independiente de la implementación de analytics 
del cotizador SOAT de Pacífico Seguros, una de las principales 
aseguradoras del Perú. El objetivo es identificar gaps en la captura 
de datos del funnel de cotización, diseñar la solución técnica para 
cerrarlos, y traducir el impacto a decisiones de negocio concretas.

Este proyecto fue elaborado con fines demostrativos y de portafolio 
profesional, sin vínculo contractual con Pacífico Seguros. La auditoría 
se realizó únicamente mediante inspección de tráfico propio con 
herramientas públicas, sin acceso a información interna de la empresa.

---

## Herramienta identificada

Google Analytics 4 (GA4) vía Google Tag Manager — Measurement Protocol v2.

---

## Hallazgos principales

**Gap 1 — Intento de pago no capturado**
El clic en "Pagar en línea" no dispara ningún evento. Pacífico no 
puede medir cuántos usuarios manifiestan intención real de compra 
ni diagnosticar la caída entre cotización y pago.

**Gap 2 — Cotizaciones no completadas sin diagnóstico**
Los estados no exitosos del funnel (vehículo no registrado, placa 
inválida, error de validación) se registran como visualizaciones 
genéricas de formulario, sin identificar el motivo. Las causas de 
abandono en el paso de cotización son invisibles.

**Gap 3 — Monto capturado fuera del estándar de ecommerce**
El monto de cotización se captura como parámetro custom 
(`montoCompraSOAT`) en lugar de usar los parámetros nativos de 
ecommerce de GA4 (`currency`, `value`, `items`). Esto limita la 
atribución de ingresos por campaña y la integración con Google Ads.

---

## Lo que este proyecto demuestra

- Inspección técnica de implementaciones de analytics en producción
- Lectura e interpretación de requests de GA4 en Chrome DevTools
- Diseño de soluciones con payload técnico listo para implementar
- Aplicación de la Ley 29733 de Protección de Datos Personales del Perú
- Traducción de gaps técnicos a impacto de negocio para stakeholders

---

## Estructura del documento

- Sección 0: Nota metodológica y principios de diseño
- Sección 1: Contexto y alcance
- Sección 2: Auditoría de la implementación actual
- Sección 3: Diagnóstico de gaps
- Sección 4: Diseño de la solución con plan de migración
- Sección 5: Impacto de negocio

---

## Autor

**Luis Alvaro Mendoza Silva**
Digital Analytics Specialist | Adobe Analytics · GTM · GA4 | 
Fintech & Insurance

[LinkedIn](https://www.linkedin.com/in/luisalvaromendozasilva-digitalanalytics)

---

> Este proyecto es parte de un portafolio de analytics digital 
> enfocado en banca y seguros en Perú.
