# WorkHub IR – INFINIX

Este proyecto es una **plataforma web ligera y gratuita** montada en **GitHub Pages** que permite acceder a tres formularios de JotForm para la gestión de visitas, creación de puntos de venta y verificación de IMEIS, integrando geolocalización y optimización para smartphones.

---

## **Estructura del proyecto**

### **Páginas principales**

1. **`index.html`**  
   - Pantalla principal tipo menú futurista.  
   - Fondo abstracto verde (`Fondo_Index.webp`).  
   - Botones futuristas degradados para redirigir a las subpáginas:
     1. Visit Check
     2. Creación POS
     3. Verificador IMEIS  
   - Título: `WorkHub IR – INFINIX`.  
   - Versión: `V.3.01` en esquina inferior derecha.  
   - Optimizado para **uso en smartphones**.

---

2. **`visitcheck.html`**  
   - Formulario **VisitCheck** embebido:  
     `https://form.jotform.com/251687013967668`  
   - Captura geolocalización y pasa los datos mediante **parámetros URL**:  
     - `latitud`
     - `longitud`
   - Fondo blanco.
   - Botón **“Regresar al WorkHub”** ubicado al **final del scroll**, centrado horizontalmente.

---

3. **`creacionpos.html`**  
   - Formulario **Creación de Punto de Venta** embebido:  
     `https://form.jotform.com/251146528825662`  
   - Captura geolocalización con campos específicos para no interferir con VisitCheck:  
     - `latitud_1`
     - `longitud_1`
   - **Permisos de cámara** habilitados para funcionalidades del formulario (ej. escáner QR o fotos).  
   - Fondo blanco.
   - Botón **“Regresar al WorkHub”** ubicado al **final del scroll**, centrado horizontalmente.

---

4. **`verificador.html`**  
   - Formulario **Verificador IMEIS** embebido:  
     `https://form.jotform.com/222794064103047`  
   - No requiere geolocalización ni cámara.  
   - Fondo blanco.
   - Botón **“Regresar al WorkHub”** ubicado al **final del scroll**, centrado horizontalmente.

---

## **Características técnicas**

- **Fuentes**: Montserrat Bold desde Google Fonts.  
- **Diseño futurista** con degradados verdes y sombras suaves.  
- **Optimizado para móviles** (layout responsive y botones adaptados).  
- **Uso de WebP** en el fondo para **optimizar peso y carga rápida**.  
- **Permisos**:
  - Geolocalización: VisitCheck y Creación POS.
  - Cámara: Creación POS.

---

## **IDs y campos importantes**

- **VisitCheck**  
  Formulario: `https://form.jotform.com/251687013967668`  
  Campos URL: `latitud`, `longitud`

- **Creación POS**  
  Formulario: `https://form.jotform.com/251146528825662`  
  Campos URL: `latitud_1`, `longitud_1`  

- **Verificador IMEIS**  
  Formulario: `https://form.jotform.com/222794064103047`  
  Sin geolocalización ni cámara.

---

## **Flujo de uso**

1. Usuario ingresa a `index.html` (WorkHub IR – INFINIX).  
2. Selecciona el formulario deseado:  
   - **Visit Check** → formulario con geolocalización (latitud/longitud).  
   - **Creación POS** → formulario con geolocalización (latitud_1/longitud_1) y cámara.  
   - **Verificador IMEIS** → formulario sin geolocalización.  
3. Completa el formulario y puede regresar al menú mediante el botón al final del scroll.

---

## **Optimización y consumo**

- **GitHub Pages** no cuenta con un límite estricto de tráfico para proyectos personales, pero optimizamos:  
  - Fondos en formato **WebP** (peso < 200 KB).  
  - Archivos HTML ligeros (< 10 KB cada uno).  
- El peso total del sitio es inferior a **250 KB** (sin contar contenido dinámico de JotForm).  
- Formularios JotForm se cargan desde sus servidores, por lo que **no consumen ancho de banda de GitHub**.

---

## **Próximos pasos posibles**

- Integración de **menú desplegable** o animaciones futuristas.  
- **Versionado** visible en el footer para control de actualizaciones.  
- Posible **modo oscuro/claro** según configuración del dispositivo.  
- Documentación sobre **cambios futuros** y escalabilidad para más formularios.
