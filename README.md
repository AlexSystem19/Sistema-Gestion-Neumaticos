# Sistema de Gestión de Neumáticos (SGNEUMA)  
  
Aplicación Power Apps para la gestión integral de inspecciones de neumáticos con capacidades offline y sincronización con SharePoint.  
  
## 🚀 Características Principales  
  
- **Inspección Offline**: Realiza inspecciones sin conexión a internet  
- **Sincronización Automática**: Sincroniza datos con SharePoint cuando hay conexión  
- **Gestión de Historial**: Consulta inspecciones previas y tendencias de desgaste  
- **Cálculos Automáticos**: Proyección de vida útil y fechas de reemplazo  
- **Interfaz Optimizada**: Diseño responsive para tablet y desktop  
  
## 📱 Arquitectura de la Aplicación  
  
### Pantallas Principales  
| Pantalla | Funcionalidad |  
|----------|---------------|  
| `Incio` | Dashboard principal y menú de navegación |  
| `sc_NuevaInspeccion_Datos` | Ingreso de placa y kilometraje |  
| `sc_NuevaInspeccion_Unidad` | Medición y cálculo de neumáticos |  
| `sc_InspeccionGuardada` | Resumen de inspección local |  
| `sc_Sincronizar` | Subida de datos a SharePoint |  
| `sc_Historial` | Navegación por historial local |  
| `sc_Buscar` | Búsqueda filtrada por placa |  
| `sc_Configuracion` | Configuración del sistema y datos de usuario |  
  
### Configuración Técnica  
- **Form Factor**: Desktop/Tablet (1366x768) [1](#0-0)   
- **Orientación**: Landscape bloqueada  
- **Runtime**: Power Apps v1.331+  
- **Estructura**: MSAppStructureVersion 2.4.0  
  
## ⚙️ Configuración  
  
### Requisitos Previos  
- Licencia de Power Apps  
- Acceso a SharePoint Online  
- Tableta o dispositivo desktop con resolución mínima 1366x768  
  
### Instalación  
1. Clonar este repositorio  
2. Importar el archivo `.msapp` en Power Apps Studio  
3. Configurar la conexión a SharePoint  
4. Publicar la aplicación  
  
## 📸 Capturas de Pantalla  
  
### Dashboard Principal  
<img width="1450" height="818" alt="Dashboard Principal" src="https://github.com/user-attachments/assets/64441302-68dc-49a6-8488-06754c0b771c" />  
  
### Nueva Inspección - Datos del Vehículo  
<img width="1446" height="814" alt="Nueva Inspección - Datos" src="https://github.com/user-attachments/assets/8ccfa9bd-e691-4bbe-9555-85bec6d79c96" />  
  
### Medición de Neumáticos  
<img width="1452" height="820" alt="Medición de Neumáticos" src="https://github.com/user-attachments/assets/3d7b8168-ac40-4bc8-bdb4-cf7fa7f43ab3" />  
  
### Resumen de Inspección  
<img width="1449" height="817" alt="Resumen de Inspección" src="https://github.com/user-attachments/assets/fdd87a32-256e-4b55-969a-ad9cc0af77a1" />  
  
### Sincronización de Datos  
<img width="1446" height="814" alt="Sincronización" src="https://github.com/user-attachments/assets/69d3813b-6974-4d31-a8bd-df3597897b93" />  
  
### Historial de Inspecciones  
<img width="1447" height="810" alt="Historial" src="https://github.com/user-attachments/assets/43040728-249b-45c7-b7fd-9026d2c9a4c3" />  
  
### Búsqueda de Inspecciones  
<img width="1445" height="821" alt="Búsqueda" src="https://github.com/user-attachments/assets/374307b8-3ef2-4544-b2b9-60451d365735" />  
  
### Configuración del Sistema  
<img width="1450" height="818" alt="Configuración" src="https://github.com/user-attachments/assets/d75f7d85-7406-429a-bf5a-20433c696b12" />  
  
### Vista Detallada de Neumático  
<img width="1449" height="813" alt="Detalle Neumático" src="https://github.com/user-attachments/assets/84e8c32a-de12-443f-80b4-10b37d2ee36a" />  
  
## 🔧 Características Técnicas  
  
### Capacidades Offline  
- `SaveData`/`LoadData` habilitados para almacenamiento local [2](#0-1)   
- Soporte expandido para colecciones complejas  
- Límites de almacenamiento forzados para estabilidad  
  
### Optimizaciones de Rendimiento  
- Carga diferida de pantallas (`delayloadscreens`) [3](#0-2)   
- Prefetch de datos de fórmulas  
- Inicio no bloqueante de la aplicación  
  
## 📊 Flujo de Trabajo  
  
```mermaid  
graph TD  
    A[Inicio] --> B[Nueva Inspección]  
    B --> C[Ingresar Datos Vehículo]  
    C --> D[Medir Neumáticos]  
    D --> E[Guardar Localmente]  
    E --> F{¿Hay Conexión?}  
    F -->|Sí| G[Sincronizar con SharePoint]  
    F -->|No| H[Consultar Historial Local]  
    G --> I[Inspección Completada]  
    H --> I
