<button href="https://github.com/labrujasiete/app-bc-ux/blob/main/casos_de_uso.md" style="font-weight: 500; font-size: 16px; padding: 10px 20px; border-radius: 9px; border: none; color: #313131">Casos de uso</button>


# Reporte UX – AppBC

## 🎯 1. Resumen Ejecutivo

**Objetivo de la app**  
Facilitar el acceso digital seguro y centralizado de los ciudadanos de Baja California a documentos oficiales como licencia de conducir, tarjeta de circulación, INE, comprobantes de domicilio y brindar acceso a la Cartelera Cultural estatal, todo desde un solo lugar, con inicio de sesión mediante LlaveBC y acceso rápido con biometría.

---

## 👥 2. Públicos objetivo

- **Ciudadanos de Baja California**
  - Adultos con licencia y vehículo propio.
  - Usuarios con smartphone Android o iOS.
  - Necesitan rápido acceso a documentos oficiales para trámites, verificaciones, etc.

- **Funcionarios**
  - (Pendiente)

---

## 📱 3. Flujos de usuario principales

### 🗝 3.1 Onboarding e inicio de sesión (Primera vez)

1. **Splash screen**
   - Logo Gobierno de BC y AppBC.
   - Breve tagline: *“Tu identidad y documentos oficiales, siempre contigo”*.

2. **Pantalla de inicio de sesión**
   - Botón principal: *“Iniciar sesión con LlaveBC”* (estilo claro y prominente).
   - Breve texto explicativo debajo: *“LlaveBC es tu acceso seguro a servicios del estado de Baja California”*.
   - Opción de ayuda: *“¿Qué es LlaveBC?”* (modal breve).

3. **Autenticación con LlaveBC**
   - Redirección o WebView al flujo oficial LlaveBC.
   - Confirmación de inicio de sesión exitoso.

4. **Registro de información faltante (primer uso)**
   - Pantalla: *“Completa tu perfil”*.
   - Campos requeridos:
     - Foto de perfil (opcional pero recomendado).
     - Comprobante de domicilio (subida o foto).
     - INE (subida o foto de ambos lados).
   - Progreso visual (paso 1 de 3, etc.) para reducir ansiedad de proceso largo.
   - Confirmación final: *“¡Listo! Tu cuenta ha sido configurada correctamente.”*

---

### 🔐 3.2 Inicio de sesión subsecuente

1. **Splash screen breve**.
2. **Autenticación biométrica**
   - Huella digital o Face ID.
3. **Redirección automática a Home/Perfil**.

---

### 🏠 3.3 Home / Perfil (Pantalla principal)

- Encabezado con nombre completo del usuario y foto de perfil.  
- **Tarjeta principal (credencial digital BC)**
  - Incluye:
    - Nombre completo
    - CURP
    - QR para verificación oficial
    - Logo Gobierno de BC
    - Fecha de emisión/actualización
- **Sección de documentos:**
  - **Licencia de conducir**
    - Vista tipo tarjeta digital, con detalles (vigencia, clase, número).
  - **Tarjeta de circulación**
    - Información básica del vehículo y QR para verificación.
  - **INE**
    - Imagen frontal y posterior.
  - **Comprobante de domicilio**
    - Última versión cargada, editable.

- **Cartelera Cultural**
  - Preview de eventos (máx. 2 visibles en home) con botón *“Ver más”*.

---

### 📂 3.4 Drawer / Navbar

- Icono hamburguesa abre el Drawer con:
  - Inicio / Perfil
  - Configuración
  - Política de privacidad
  - Cerrar sesión (con confirmación modal)

---

### ⚙️ 3.5 Configuración

- Editar foto de perfil
- Editar información de contacto
- Cambiar comprobante de domicilio
- Ver términos y condiciones
- Ayuda / FAQ

---


## 🔍 4. Funcionalidades futuras (sugerencias)

✅ **Verificación por QR**  
Funcionarios pueden escanear el QR en la credencial digital del ciudadano para validar documentos en tiempo real.

✅ **Descarga offline**  
Permitir guardar versión cifrada de documentos para consulta sin internet.

✅ **Notificaciones push**  
Recordatorios de vencimiento de licencia, tarjeta de circulación o eventos de cartelera cultural.

✅ **Integración con otros servicios estatales**  
Como pagos de derechos vehiculares, citas en línea, etc.

✅ **Modo oscuro**  
Para ahorro energético y confort visual.

---

## 🔒 5. Seguridad

- Uso estricto de autenticación LlaveBC.
- Cifrado local de documentos y datos sensibles.
- Bloqueo con biometría cada vez que se sale de la app o después de 5 min inactiva.
- Ocultar información en vista de apps recientes (flag de seguridad en Android / iOS).

---

## 💡 6. Conclusiones y siguientes pasos

✅ Realizar **wireframes y prototipos** de cada pantalla para pruebas de usabilidad.  
✅ Definir con el área legal los disclaimers necesarios sobre documentos digitales.  
✅ Realizar sesiones de **pruebas con usuarios reales** (ciudadanos adultos de BC) para validar flujo de onboarding y percepción de legitimidad de documentos digitales.  
✅ Revisar identidad gráfica oficial de Gobierno de BC para garantizar cumplimiento de lineamientos institucionales.

---

### ✨ **Siguientes entregables**

- Wireframes de cada pantalla  
- Especificaciones de componentes UI  
- Flowcharts diagramados  
- User stories y casos de uso

---