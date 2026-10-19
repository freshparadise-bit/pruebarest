# PROPUESTA COMERCIAL Y ESTRATÉGICA DE SOLUCIÓN TECNOLÓGICA POS & GESTIÓN DE PEDIDOS
**Cliente:** Restaurante / Food Truck Tropical "JIQUI" (Cocles, Puerto Viejo)  
**Preparado por:** Consultoría & Dirección Comercial Tecnológica  
**Fecha:** 16 de Octubre, 2026  
**Formato de Entrega:** Aplicación Web Autónoma PWA / Standalone (Zero-Server / Serverless Offline-Ready) + Sincronización Exclusiva con Google Sheets

---

## 1. RESUMEN EJECUTIVO & PROPÓSITO DE VALOR
El presente proyecto entrega una solución de software integral, ágil y de alto impacto visual diseñada específicamente para la operativa dinámica del restaurante/food truck "JIQUI" en Puerto Viejo de Talamanca. 

### Beneficios Clave del Negocio:
1. **Datos Reales y Limpios (Sin Registros Fantasma de Prueba):**  
   Se removieron por completo todas las órdenes de prueba, ventas falsas y platillos ficticios. El sistema inicia en blanco y **carga estrictamente los usuarios y menú creados en su Google Sheet**.
2. **Acceso Obligatorio con Login y Contraseña:**
   - La pantalla de inicio exige un usuario y contraseña válidos antes de permitir ver cualquier área del sistema.
   - Cuenta Máster predeterminada de alta seguridad para configuración inicial: **Usuario:** `admin` | **Contraseña:** `987654`.
3. **Gestión y Carga de Usuarios desde Google Sheets:**
   - Hoja `Usuarios`: Columnas **Nombre**, **Contraseña** y **Tipo** (*mesero*, *cocina*, *caja* o *master*).
   - El POS descarga esta lista en tiempo real para autorizar los inicios de sesión.
4. **Catálogo de Menú Alimentado desde Google Sheets:**
   - Hoja `Menu_Productos`: Los platillos, smoothies, caldosas y snacks se definen en la hoja de cálculo y se cargan automáticamente en el botón de comanda de los meseros.
5. **Perfilado y Seguridad al 100% por Roles:**  
   - **Mesero:** Acceso único y exclusivo a la pestaña de **Mesas (Toma de pedidos y cobro)**.
   - **Cocina (KDS):** Acceso único y exclusivo a la pestaña de **Cocina**. No ve precios ni caja.
   - **Caja:** Acceso a **Mesero, Cocina y Caja**.
   - **Máster:** Acceso total a las 4 pestañas (**Mesero, Cocina, Caja y Máster**), creación de usuarios y catálogo.
6. **Almacenamiento Continuo en Google Sheets:**  
   - `Usuarios`: Lista de operadores autorizados.
   - `Menu_Productos`: Catálogo oficial de platillos y precios en colones.
   - `Comandas`: Órdenes reales enviadas a cocina con detalle de productos y notas.
   - `Ventas_Cobros`: Facturación en colones y dólares con vueltos entregados.
   - `Cancelaciones`: Auditoría con justificación obligatoria.

---

## 2. GUÍA DE INSTALACIÓN RÁPIDA DE GOOGLE SHEETS
1. En Google Drive cree una hoja llamada **"JIQUI - Ventas y Operación POS"**.
2. Vaya a **Extensiones > Apps Script**.
3. Pegue el código de **`GOOGLE_SHEETS_SCRIPT.gs`** y haga clic en **Implementar > Nueva Implementación** (Tipo Web App, acceso "Cualquier usuario").
4. Copie la URL `/exec` y péguela en el botón **"🔗 Conectar / Configurar Sheets"** en la pantalla de login de **`index.html`**.
5. Presione **"🔄 Sincronizar de Sheets"** y el sistema cargará al instante todos sus usuarios y menú real.
