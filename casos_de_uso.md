<button href="https://github.com/labrujasiete/app-bc-ux/blob/main/readme.md" style="font-weight: 500; font-size: 16px; padding: 10px 20px; border-radius: 9px; border: none; color: #313131">Reporte UX</button>

# 📄 Casos de Uso – AppBC

## 🎯 Resumen

Este documento describe los casos de uso principales para la AppBC, que permitirá a los ciudadanos de Baja California acceder de forma digital y segura a sus documentos oficiales, así como funcionalidades complementarias.

---

## 👥 Actores

- **Ciudadano:** Usuario principal que consulta y gestiona sus documentos digitales.
- **Funcionario/Verificador:** Persona que valida documentos presentados por ciudadanos (futuro).
- **Sistema LlaveBC:** Sistema de autenticación estatal para inicio de sesión seguro.
- **AppBC:** Aplicación móvil Android/iOS objeto de este análisis.

---

## 📑 Lista de Casos de Uso

| ID | Nombre |
| --- | --- |
| CU01 | Inicio de sesión con LlaveBC |
| CU02 | Registro de información adicional (primer uso) |
| CU03 | Autenticación biométrica (usos subsecuentes) |
| CU04 | Visualizar credencial digital BC |
| CU05 | Visualizar licencia de conducir digital |
| CU06 | Visualizar tarjeta de circulación digital |
| CU07 | Visualizar INE digital |
| CU08 | Visualizar comprobante de domicilio |
| CU09 | Acceder a Cartelera Cultural |
| CU10 | Editar perfil de usuario |
| CU11 | Cambiar comprobante de domicilio |
| CU12 | Cerrar sesión |
| CU13 | Ver política de privacidad |
| CU14 | Escanear QR de credencial (futuro) |
| CU15 | Descargar documentos para uso offline (futuro) |

---

### 📌 CU01 – Inicio de sesión con LlaveBC

- **Actor:** Ciudadano
- **Descripción:** El ciudadano inicia sesión en la app utilizando su cuenta LlaveBC.
- **Precondición:** El usuario tiene cuenta LlaveBC activa.
- **Flujo principal:**
  1. Usuario abre la app.
  2. Pantalla de inicio muestra botón “Iniciar sesión con LlaveBC”.
  3. Usuario pulsa el botón.
  4. Sistema redirige a flujo de autenticación LlaveBC (WebView o navegador).
  5. LlaveBC autentica usuario.
  6. Sistema recibe respuesta exitosa y redirige a registro de información adicional si es primer inicio, o a Home si no.
- **Postcondición:** Usuario autenticado en AppBC.

---

### 📌 CU02 – Registro de información adicional (primer uso)

- **Actor:** Ciudadano
- **Descripción:** Al iniciar sesión por primera vez, se solicita información adicional para completar su perfil.
- **Precondición:** Usuario autenticado por LlaveBC.
- **Flujo principal:**
  1. Sistema detecta primer inicio.
  2. Muestra pantalla de registro de información adicional.
  3. Usuario sube o toma foto de su comprobante de domicilio.
  4. Usuario sube o toma foto de su INE (frente y reverso).
  5. Usuario sube o toma foto de perfil (opcional).
  6. Usuario confirma.
  7. Sistema guarda la información en la base de datos.
  8. Muestra mensaje de confirmación: “Tu cuenta está lista”.
- **Postcondición:** Perfil completado y usuario redirigido a Home.

---

### 📌 CU03 – Autenticación biométrica (usos subsecuentes)

- **Actor:** Ciudadano
- **Descripción:** El usuario accede a la app usando biometría configurada en su dispositivo.
- **Precondición:** Usuario ya inició sesión al menos una vez y tiene biometría configurada en su teléfono.
- **Flujo principal:**
  1. Usuario abre la app.
  2. Sistema solicita autenticación biométrica (huella o Face ID).
  3. Usuario autoriza.
  4. Sistema valida y muestra Home/Perfil.
- **Postcondición:** Usuario autenticado y en Home.

---

### 📌 CU04 – Visualizar credencial digital BC

- **Actor:** Ciudadano
- **Descripción:** El usuario visualiza su credencial digital creada por AppBC con QR de verificación.
- **Precondición:** Usuario autenticado.
- **Flujo principal:**
  1. Usuario ingresa a Home.
  2. Sistema muestra tarjeta de credencial digital con nombre, CURP, foto, QR de verificación y fecha de emisión.
- **Postcondición:** Usuario visualiza su credencial.

---

### 📌 CU05 – Visualizar licencia de conducir digital

- **Actor:** Ciudadano
- **Descripción:** Visualiza la versión digital de su licencia de conducir.
- **Precondición:** Usuario autenticado.
- **Flujo principal:**
  1. Usuario accede a la sección Licencia de Conducir.
  2. Sistema muestra tarjeta con número de licencia, clase, vigencia y QR (si aplica).
- **Postcondición:** Usuario visualiza su licencia digital.

---

### 📌 CU06 – Visualizar tarjeta de circulación digital

- **Actor:** Ciudadano
- **Descripción:** Visualiza su tarjeta de circulación de vehículo.
- **Precondición:** Usuario autenticado.
- **Flujo principal:**
  1. Usuario accede a la sección Tarjeta de Circulación.
  2. Sistema muestra detalles del vehículo y QR de verificación.
- **Postcondición:** Usuario visualiza su tarjeta de circulación digital.

---

### 📌 CU07 – Visualizar INE digital

- **Actor:** Ciudadano
- **Descripción:** Consulta su INE digital almacenada.
- **Precondición:** Usuario autenticado y con INE previamente cargada.
- **Flujo principal:**
  1. Usuario ingresa a la sección INE.
  2. Sistema muestra imagen frontal y posterior.
- **Postcondición:** Usuario visualiza su INE digital.

---

### 📌 CU08 – Visualizar comprobante de domicilio

- **Actor:** Ciudadano
- **Descripción:** Consulta su comprobante de domicilio cargado.
- **Precondición:** Usuario autenticado y con comprobante cargado.
- **Flujo principal:**
  1. Usuario ingresa a la sección Comprobante de domicilio.
  2. Sistema muestra el último comprobante cargado.
- **Postcondición:** Usuario visualiza su comprobante.

---

### 📌 CU09 – Acceder a Cartelera Cultural

- **Actor:** Ciudadano
- **Descripción:** Consulta los eventos culturales disponibles.
- **Precondición:** Usuario autenticado.
- **Flujo principal:**
  1. Usuario ingresa a sección Cartelera Cultural desde Home o Drawer.
  2. Sistema muestra listado de eventos y detalles.
- **Postcondición:** Usuario visualiza la cartelera.

---

### 📌 CU10 – Editar perfil de usuario

- **Actor:** Ciudadano
- **Descripción:** Modifica su foto de perfil o información personal editable.
- **Precondición:** Usuario autenticado.
- **Flujo principal:**
  1. Usuario ingresa a Configuración.
  2. Selecciona Editar Perfil.
  3. Realiza cambios y guarda.
- **Postcondición:** Información actualizada en base de datos.

---

### 📌 CU11 – Cambiar comprobante de domicilio

- **Actor:** Ciudadano
- **Descripción:** Actualiza su comprobante de domicilio.
- **Precondición:** Usuario autenticado.
- **Flujo principal:**
  1. Usuario ingresa a Configuración.
  2. Selecciona Cambiar comprobante de domicilio.
  3. Sube nuevo archivo o toma foto.
  4. Confirma y sistema actualiza.
- **Postcondición:** Nuevo comprobante registrado.

---

### 📌 CU12 – Cerrar sesión

- **Actor:** Ciudadano
- **Descripción:** Finaliza su sesión actual.
- **Precondición:** Usuario autenticado.
- **Flujo principal:**
  1. Usuario abre Drawer.
  2. Selecciona “Cerrar sesión”.
  3. Sistema solicita confirmación.
  4. Usuario confirma.
  5. Sistema cierra sesión y muestra pantalla de inicio.
- **Postcondición:** Sesión finalizada.

---

### 📌 CU13 – Ver política de privacidad

- **Actor:** Ciudadano
- **Descripción:** Consulta la política de privacidad de la app.
- **Precondición:** Usuario autenticado.
- **Flujo principal:**
  1. Usuario abre Drawer.
  2. Selecciona “Política de privacidad”.
  3. Sistema muestra contenido en pantalla o WebView.
- **Postcondición:** Usuario lee política de privacidad.

---

### 📌 CU14 – Escanear QR de credencial (futuro)

- **Actor:** Funcionario/Verificador
- **Descripción:** Funcionario escanea el QR de la credencial digital del ciudadano para validar su autenticidad.
- **Precondición:** Funcionario con app verificador y permisos.
- **Flujo principal:**
  1. Funcionario abre app verificador.
  2. Selecciona opción Escanear QR.
  3. Escanea QR de la credencial digital.
  4. Sistema valida y muestra datos verificados.
- **Postcondición:** Documento validado.

---

### 📌 CU15 – Descargar documentos para uso offline (futuro)

- **Actor:** Ciudadano
- **Descripción:** Descarga documentos cifrados para acceso sin conexión.
- **Precondición:** Usuario autenticado.
- **Flujo principal:**
  1. Usuario selecciona documento.
  2. Toca opción “Disponible sin conexión”.
  3. Sistema descarga versión cifrada.
- **Postcondición:** Documento accesible offline con biometría.

---

## ✅ Conclusión

Estos casos de uso cubren la funcionalidad principal y futura de la AppBC para un desarrollo ágil y planificación de sprints, priorizando la experiencia ciudadana y la seguridad de los documentos oficiales.

---