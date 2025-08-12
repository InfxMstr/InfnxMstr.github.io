# WorkHub IR – INFINIX

Versión actual: **V.3.01**

Proyecto web gratuito alojado en **GitHub Pages** para centralizar accesos a formularios Jotform usados en la operación de Infinix Mobility en Colombia. El sistema incluye integración con **geolocalización GPS** y permisos de cámara cuando es necesario.

---

## 📂 Estructura de páginas

### **1. Index (Página principal)**
- **Fondo:** Imagen `Fondo_Index.webp` con `background: center/cover no-repeat`.
- **Tipografía:** Fuente **Montserrat** peso 700 (negrita) importada desde Google Fonts.
- **Botones:**  
  1. **Visit Check** → `visitcheck.html`  
  2. **Creación POS** → `creacionpos.html`  
  3. **Verificador IMEIS** → `verificador.html`  
  4. **Control de Sell Out** → `controlsellout.html`  

  **Estilo botones:**  
  - Degradado verde (`#00ff88` → `#006644`).  
  - Bordes redondeados de 12px.  
  - Sombra verde.  
  - Hover: aumenta escala y sombra.  

- **Versión:** Texto pequeño (`0.75rem`) en esquina inferior derecha, color `#aaa`, estilo *italic*.

---

### **2. VisitCheck**
- **Formulario:** [https://form.jotform.com/251687013967668](https://form.jotform.com/251687013967668)  
- **Permisos iframe:** `allow="geolocation"`.
- **Geolocalización:** Script obtiene `latitud` y `longitud` y los pasa como parámetros a la URL del formulario.
- **Fondo:** Blanco (`#fff`).
- **Botón de regreso:**  
  - Texto: `"Regresar al WorkHub"`.  
  - Estilo: `inline-block`, margen vertical, fondo `rgba(0, 255, 100, 0.1)`, borde `#00ff88`, texto `#00aa55`, padding pequeño, bordes redondeados 8px, `backdrop-filter: blur(5px)`, hover con más opacidad.

---

### **3. Creación POS**
- **Formulario:** [https://form.jotform.com/251146528825662](https://form.jotform.com/251146528825662).  
- **Permisos iframe:** `allow="geolocation; camera"`.
- **Geolocalización:** Script obtiene `latitud_1` y `longitud_1` como parámetros.
- **Estilo de página y botón:** Igual a VisitCheck.

---

### **4. Verificador de IMEIS**
- **Formulario:** [https://form.jotform.com/222794064103047](https://form.jotform.com/222794064103047)  
- **Permisos iframe:** `allow="camera"`.
- **Sin geolocalización**.
- **Estilo de página y botón:** Igual a VisitCheck.

---

### **5. Control de Sell Out**
- **Formulario:** [https://form.jotform.com/243044313856656](https://form.jotform.com/243044313856656) 
- **Permisos iframe:** `allow="camera"`.
- **Sin geolocalización**.
- **Estilo de página y botón:** Igual a VisitCheck.

---

## 🖥️ Lógica de geolocalización
Se usa `navigator.geolocation.getCurrentPosition` para capturar coordenadas y reconstruir la URL del iframe agregando los parámetros requeridos:
```javascript
navigator.geolocation.getCurrentPosition(function(pos) {
  var lat = pos.coords.latitude;
  var lon = pos.coords.longitude;
  var iframe = document.getElementById('formulario');
  iframe.src = `FORM_URL?latitud=${lat}&longitud=${lon}`;
});
