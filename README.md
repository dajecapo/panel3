# Sección: Testimonios de Usuarios (Panel de Administración)

Esta sección del Panel de Administración permite visualizar, aprobar o eliminar los testimonios enviados por usuarios a través del formulario público de la sección “Testimonios de Usuarios”. Está conectada en tiempo real con la pestaña `TESTIMONIOS` de la hoja de cálculo principal del sistema.

## ✅ Funcionalidades principales

- Visualización de todos los testimonios enviados.
- Botones de **Aprobar** y **Eliminar** por fila.
- Lectura directa desde la pestaña `TESTIMONIOS` de Google Sheets.
- Actualización en tiempo real de los cambios reflejados en la hoja.
- Interfaz clara, ordenada y compatible con dispositivos móviles.

## 📄 Estructura esperada en Google Sheets

La pestaña `TESTIMONIOS` debe tener los siguientes encabezados, en este orden exacto (todo en minúsculas y sin tildes):


> ⚠️ El orden y el nombre exacto de los encabezados son indispensables para que el panel funcione correctamente.

## 🔗 Lógica de conexión

Esta sección se conecta a través del parámetro `tipo=testimonios` al Web App de Google Apps Script publicado. Así se garantiza que el sistema lea únicamente los datos de la hoja `TESTIMONIOS`.

### Ejemplo de llamada directa:


## ⚙️ Acciones disponibles

- **Aprobar:** Cambia el valor de la columna `estatus` a `"aprobado"`.
- **Eliminar:** Elimina permanentemente la fila seleccionada de la hoja.

Estas acciones se ejecutan mediante el método `doPost()` en Apps Script, utilizando los parámetros `fila`, `accion` y `tipo`.

## 🧪 Verificación técnica

- [x] Función `doGet()` diferenciando correctamente `tipo=testimonios`.
- [x] Función `doPost()` con columna de estatus en la posición correcta (columna 5).
- [x] Botones del panel conectados y funcionando.
- [x] Cambios reflejados en la hoja de cálculo sin errores.

## 🧼 Recomendaciones

- No cambiar los nombres ni el orden de las columnas en la pestaña `testimonios`.
- Actualizar el Apps Script y desplegar una nueva versión si se realizan cambios futuros.
- Revisar regularmente la hoja para detectar spam o envíos maliciosos, aunque el formulario ya cuenta con captcha.

---

Esta sección forma parte del sistema integral **Adopta un Sabio**, cuyo objetivo es valorar y compartir la sabiduría de los adultos mayores mediante el testimonio y la interacción con jóvenes.
