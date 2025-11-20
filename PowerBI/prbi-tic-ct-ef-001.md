<!-- ========================================================= -->
<!--   MANUAL ISO 9001 – FORMATO OFICIAL (VERSIÓN MARKDOWN)   -->
<!-- ========================================================= -->

---
# **MANUAL DEL PROCESO – GENERACIÓN, VALIDACIÓN Y PUBLICACIÓN DE INFORMACIÓN FINANCIERA EN POWER BI**  
**Código:** PRBI-TIC-CT-EF-001  
**Versión:** 1.0  
**Norma:** ISO 9001:2015  
**Estado:** Vigente  
**Nivel de difusión:** Interno Controlado  

---

## **ENCABEZADO**  
| **Nombre del Documento** | Manual del Proceso de Generación, Validación y Publicación de Información Financiera en Power BI |
|--------------------------|---------------------------------------------------------------------------------------------------|
| **Código** | PRBI-TIC-CT-EF-001 |
| **Versión** | 1.0 |
| **Fecha de Emisión** | 2025-11-15 |
| **Propietario del Proceso** | CIO – Área de Tecnología |
| **Áreas Involucradas** | Tecnología – Contabilidad |
| **Norma Aplicable** | ISO 9001:2015 |
| **Clasificación** | Procedimiento Corporativo |
| **Difusión** | Interno Controlado |

---

# **1. OBJETIVO**
Definir el proceso corporativo para la extracción, transformación, validación, certificación y publicación de información financiera en Power BI, garantizando:

- Integridad, trazabilidad y precisión.
- Separación clara de roles entre Tecnología, Contabilidad y Revisoría Fiscal.
- Cumplimiento de la Norma ISO 9001:2015.
- Control documental, auditorías y mejora continua.

---

# **2. ALCANCE**
Este procedimiento aplica a todas las compañías del grupo empresarial y cubre:

- Procesos ETL desde ERP, SQL, archivos y APIs.  
- Modelado y validación técnica en Power BI Desktop.  
- Publicación y control en Power BI Service.  
- Validación contable previa y auditoría fiscal posterior.

**Excluye:**  
La generación de estados financieros oficiales (responsabilidad exclusiva de Contabilidad).

---

# **3. POLÍTICA DE CALIDAD**
La organización garantiza que:

- El flujo de información financiera es **preciso, verificable y auditado**.  
- Tecnología **no genera estados financieros**; solo transforma y modela datos.  
- Contabilidad **aprueba y certifica** todas las cifras antes de su publicación.  
- Revisoría Fiscal **audita** el proceso sin intervenir en la transformación técnica.  
- Se mantiene **trazabilidad y mejora continua** en todos los pasos del proceso.

---

# **4. DEFINICIONES**
| Término | Definición |
|--------|------------|
| **Power BI** | Herramienta de análisis y visualización de datos. |
| **ETL** | Extracción, Transformación y Carga de datos. |
| **Maestros Contables** | Plan de cuentas, terceros, centros de costo, etc. |
| **Dataset** | Conjunto de datos que alimenta los modelos analíticos. |
| **Revisoría Fiscal** | Auditor independiente del proceso contable y financiero. |

---

# **5. CONTROLES DE CALIDAD**
| **Etapa** | **Control aplicado** | **Responsable** | **Evidencia** |
|-----------|----------------------|------------------|----------------|
| Extracción | Conexión a fuentes autorizadas | Tecnología | Log de extracción |
| Transformación | Validación de tipos, duplicados, nulos | Tecnología | Informe ETL |
| Modelado | Validación del modelo tabular | Tecnología | Arquitectura del modelo |
| Validación contable | Comparación con libros oficiales | Contabilidad | Formato de aprobación |
| Publicación | Publicación solo tras aprobación | Tecnología | Registro Power BI |
| Auditoría | Revisión de coherencia | Revisoría Fiscal | Informe de auditoría |

---

# **6. PROCEDIMIENTO**

## **6.1 Entradas**
- Datos oficiales del ERP  
- Libros contables consolidados  
- Catálogos maestros  
- Parámetros contables vigentes  

---

## **6.2 Actividades del Proceso (E → T → V → P → A)**

### **6.2.1 Extracción (E) — Responsable: Tecnología**
- Validar acceso a fuentes autorizadas.  
- Configurar conexiones ERP / SQL / APIs.  
- Registrar evidencias del proceso ETL.

---

### **6.2.2 Transformación (T) — Responsable: Tecnología**
- Limpieza y normalización de datos.
- Validación técnica: duplicados, nulos, tipos.
- Construcción del modelo semántico.
- Creación de medidas DAX.
- Generación del informe ETL.

---

### **6.2.3 Validación Contable (V)**  
**Responsable:** Contabilidad (A)  
**Soporte:** Tecnología (R)

- Comparación con cifras oficiales del ERP.  
- Reporte de inconsistencias.  
- Ajustes contables en caso necesario.  
- Aprobación formal mediante formato.

---

### **6.2.4 Publicación (P) — Responsable: Tecnología**
- Publicar dataset en Power BI Service.  
- Actualizar credenciales y Gateway.  
- Comunicar disponibilidad a Dirección y Contabilidad.

---

### **6.2.5 Auditoría Fiscal (A) — Responsable: Revisoría Fiscal**
- Verificar consistencia entre ERP → Dataset → Reporte.  
- Solicitar evidencias documentales.  
- Emitir informe de auditoría.

---

## **6.3 Salidas**
- Dataset certificado.  
- Dashboard publicado.  
- Evidencias completas del proceso.  
- Registro de versión y trazabilidad.

---

# **7. MATRIZ RACI**
| Actividad | Tecnología | Contabilidad | Revisoría Fiscal | Dirección | CIO |
|-----------|------------|--------------|------------------|-----------|-----|
| Cierre contable | I | **R/A** | I | I | I |
| Extracción y ETL | **R** | C | I | I | A |
| Modelado Power BI | **R** | I | I | I | A |
| Validación preliminar | C | **R** | I | I | I |
| Ajustes contables | I | **R** | I | I | I |
| Validación final | C | **A** | I | I | I |
| Aprobación fiscal | I | I | **A/R** | I | I |
| Publicación Power BI | **R** | A | I | I | I |
| Distribución del informe | C | I | I | **R** | I |
| Aprobación del proceso | I | A | I | I | **A** |

- **R**: Responsable 
- **A**: Autoridad / Aprueba 
- **C**: Consulta 
- **I**: Informa 
---

# **8. ROLES Y RESPONSABILIDADES**

### **Contabilidad**
- Dueña y certificadora de las cifras.  
- Ejecuta ajustes y emite aprobaciones.

### **Tecnología**
- Administra ETL, modelos y Power BI Service.  
- Garantiza calidad, seguridad y trazabilidad.
- Soporte sobre la herramienta Power BI.  

### **Revisoría Fiscal**
- Verifica consistencia y trazabilidad.  
- Emite informes de auditoría.

### **Dirección**
- Consume el informe para toma de decisiones.

---

# **9. ARTEFACTOS DEL PROCESO**
- Carpeta de evidencias del cierre.  
- Log ETL.  
- Archivo `.pbix` aprobado.  
- Dataset publicado en Power BI Service.  
- Registro de aprobación contable.  
- Informe de auditoría.

---

# **10. INDICADORES DE CALIDAD**

| Indicador | Objetivo | Responsable |
|-----------|----------|-------------|
| % de cargas exitosas | ≥ 98% | Tecnología |
| Tiempo aprobación contable | ≤ 3 días | Contabilidad |
| Nº de reprocesos | ≤ 1 por versión | Tecnología / Contabilidad |
| Retrasos en publicación | 0 incidentes | Tecnología |

---

# **11. DIAGRAMA BPMN (DESCRIPCIÓN TEXTUAL)**
**Pool:** Grupo Empresarial  

### **Lane: Contabilidad**
- Inicio → Cierre contable  
- Validación ERP  
- Liberación de datos  
- Revisión en Power BI  
- ¿Correcto?  
  - No → Ajuste en ERP → Reinicia ETL  
  - Sí → Aprobación final  
- Envío a Revisoría Fiscal

### **Lane: Tecnología**
- Ejecutar ETL  
- Validar calidad técnica  
- Actualizar dataset  
- Notificar a Contabilidad

### **Lane: Revisoría Fiscal**
- Revisar cifras  
- ¿Cumple?  
  - No → Solicitud de aclaraciones  
  - Sí → Aprobación fiscal

### **Lane: Dirección**
- Consulta del informe publicado  
- Fin del proceso

### **Vista Grafica del DIAGRAMA BMPM**
---
![EF](assets/img/API_NSX_2.png)
---

# **12. CONTROL DE VERSIONES**
| Versión | Fecha | Descripción | Elaboró | Aprobó |
|--------|--------|-------------|----------|---------|
| 1.0 | 2025-11-15 | Creación del procedimiento unificado bajo ISO 9001 | CIO | Contabilidad |

---

> **Documento controlado.**  
> Reproducción parcial o total prohibida sin autorización del CIO.  
> La versión vigente se encuentra en el repositorio corporativo de documentación.
---