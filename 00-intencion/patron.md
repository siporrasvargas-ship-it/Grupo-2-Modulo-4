# El patrón

> Qué se repite. Se describe con episodios que se pueden observar, no como una carencia, y dice quién gana y quién pierde con la situación actual.

# 00-intencion/patron.md — Análisis del Patrón Objetivo

## 1. ¿Qué se repite? (Episodios observables)

El patrón observable surge cuando un usuario de la Caja Costarricense de Seguro Social (CCSS) se enfrenta a un imprevisto (laboral, familiar o de salud) que le impide asistir a una cita médica previamente programada en su EBAIS de adscripción.

### Episodios concretos observables:
* **Episodio A (Reacción telefónica habitual):** El usuario busca el número de teléfono del EBAIS o Área de Salud para llamar y solicitar la cancelación. Con frecuencia experimenta líneas ocupadas o llamadas no respondidas, lo que genera frustración y abandono del intento.
* **Episodio B (Desplazamiento físico innecesario):** El usuario (o un familiar asignado) decide trasladarse presencialmente a la instalación del EBAIS o del Hospital únicamente para avisar que no asistirá o pedir una reprogramación.
* **Episodio C (Inasistencia / Ausentismo):** Al percibir que cancelar implica "hacer fila" o "llamar sin que contesten", el usuario desiste de realizar el trámite, provocando que el cupo médico se pierda por ausentismo.
* **Episodio D (Desorientación de nivel de atención):** El usuario acude o llama directamente al Hospital para gestionar un trámite que corresponde a su centro de atención primaria (EBAIS).

---

## 2. Mecanismo que sostiene el patrón

El comportamiento repetido se mantiene debido a la interacción de tres capas estructurales:

* **Reglas:** 
  * Asignación rígida de citas donde la inasistencia no genera una penalización inmediata visible para el usuario, desincentivando el esfuerzo de cancelar si el canal presenta fricción.
  * La funcionalidad de cancelación existe en la App EDUS (regla institucional), pero la notificación/recordatorio tradicional enviado por la institución no explicita este flujo ni sus pasos.
* **Prácticas:** 
  * Los usuarios operan bajo el hábito de "intermediación humana" (necesidad de hablar con una persona para sentir que el trámite quedó procesado).
  * Frente a dudas, la conducta aprendida por defecto es marcar por teléfono o enviar a un familiar presencialmente.
* **Narrativas:** 
  * *"Cancelar una cita en la CCSS es muy difícil o nadie contesta el teléfono."*
  * *"La App EDUS solo sirve para ver dictámenes o sacar citas, no para cancelarlas."*
  * *"Si no hablo con una recepcionista, la cita no queda cancelada."*

---

## 3. Distribución de valor (¿Quién gana y quién pierde con la situación actual?)

La permanencia de este patrón genera una asimetría clara en la distribución de valor y recursos dentro del sistema de salud pública:

### 🔻 Quiénes PIERDEN en la situación actual:
1. **Otros pacientes de la comunidad:** Pierden la oportunidad de acceder a un cupo médico oportunamente. Un cupo no cancelado a tiempo es una consulta médica desaprovechada.
2. **El personal administrativo y telefónico del EBAIS:** Pierde tiempo operativo gestionando llamadas repetitivas o atendiendo consultas presenciales de bajo valor que podrían auto-gestionarse.
3. **El usuario con el imprevisto:** Pierde tiempo, dinero en transportes o minutos telefónicos intentando hacer una gestión que podría resolver autónomamente.
4. **El sistema de salud (CCSS):** Pierde eficiencia operativa e incrementa la tasa de ausentismo médico en el primer nivel de atención.

### 🔺 Quiénes GANAN (o perciben un beneficio aparente) en la situación actual:
1. **El usuario en su zona de confort habitada:** Gana la "falsa seguridad" psicológica de que al hablar con una persona (o ir presencialmente) tiene certeza absoluta del trámite, evitando enfrentarse a la fricción tecnológica de recordar contraseñas o usar la app.
2. **El patrón de menor esfuerzo en el momento del imprevisto:** Si el canal tradicional falla (no contestan el teléfono), el usuario justifica éticamente el "no asistir" recargando la culpa en la falta de atención del centro de salud.

---

## 4. Evidencia de soporte
* **Datos de campo (25-Nov-2026):** Muestra de 5 usuarios donde el **80%** optó de forma espontánea por canales tradicionales (llamada/presencial en EBAIS o Hospital) y solo el **20%** contempló la autogestión en la App EDUS ([Ver registro completo](../01-investigacion/evidencias.md)).
