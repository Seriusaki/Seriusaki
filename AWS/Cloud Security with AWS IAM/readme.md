# 🛡️ Cloud Security with AWS IAM

![AWS](https://img.shields.io/badge/AWS-IAM-orange?logo=amazonaws)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-Educational-blue)
![Made with ❤️](https://img.shields.io/badge/Made%20with-%E2%9D%A4-red)

---

## 🧠 Descripción del Proyecto

Este proyecto demuestra cómo **AWS Identity and Access Management (IAM)** puede utilizarse para **controlar el acceso a instancias EC2** mediante **grupos de usuarios, políticas JSON y etiquetas (tags)**.  
El objetivo fue **aplicar el principio de privilegio mínimo**, asegurando un acceso controlado entre los entornos de **desarrollo** y **producción**.

> 💬 “Mi meta fue aprender a diseñar políticas seguras y escalables, capaces de proteger los recursos cloud aplicando gobernanza y buenas prácticas de seguridad.”

---

## 🧰 Tecnologías y Conceptos Utilizados

| Servicio / Concepto | Descripción |
|----------------------|-------------|
| **AWS IAM** | Servicio de gestión de identidades y accesos. |
| **EC2 (Elastic Compute Cloud)** | Entorno de prueba para validar permisos. |
| **Políticas JSON** | Definición detallada de reglas de acceso y condiciones. |
| **Tag-Based Access Control (ABAC)** | Control de acceso basado en etiquetas como `development` y `production`. |
| **Account Alias** | Alias personalizado para el inicio de sesión en AWS. |
| **Principio de Privilegio Mínimo** | Estrategia de seguridad para limitar el acceso solo a lo necesario. |

---

## 🗂️ Pasos del Proyecto

### 1️⃣ Configuración de las Instancias EC2
- Se crearon **dos instancias EC2** con etiquetas distintas:  
  - `Env=development`  
  - `Env=production`  
- Estas etiquetas se utilizaron como base para segmentar permisos.

---

### 2️⃣ Creación de Usuarios y Grupos IAM
- Se creó un **grupo de internos (interns)** dentro de IAM.  
- Al grupo se le asignó una **política personalizada** que regula el acceso a las instancias EC2.  
- Los usuarios individuales heredan los permisos al formar parte del grupo.

---

### 3️⃣ Diseño de la Política IAM
- La política fue desarrollada en **formato JSON**, definiendo acciones, recursos y condiciones específicas.  
- Las reglas establecían que:
  - Solo se permitan acciones sobre instancias **etiquetadas como `development`**.  
  - Los usuarios tengan acceso **de solo lectura** a todos los recursos EC2.  
  - Se **bloquee la creación o eliminación de etiquetas**.  
- Con esto se logró un **control seguro y granular** del entorno cloud.

---

### 4️⃣ Pruebas de Acceso y Validación
- Al probar con un usuario del grupo `interns`:  
  - Intento de detener la instancia de **producción** → ❌ **Acceso denegado**  
  - Intento de detener la instancia de **desarrollo** → ✅ **Acceso permitido**  
- Los resultados confirmaron la **correcta aplicación del principio de privilegio mínimo**.

---

### 5️⃣ Creación del Alias de Cuenta
- Se configuró un **account alias** para reemplazar el ID numérico con un nombre más amigable.  
- Esto facilitó el inicio de sesión mediante una URL


---

## 💡 Lecciones Aprendidas

- Diseñar políticas JSON requiere **precisión y validación continua**.  
- Las **etiquetas (tags)** son esenciales para separar entornos y gestionar accesos dinámicos.  
- El **principio de privilegio mínimo** es clave para mantener la seguridad en la arquitectura cloud.  
- Una buena **gobernanza de IAM** permite escalar infraestructuras sin comprometer la seguridad.

---

## 🧱 Relación con Arquitectura de Datos

Este proyecto refuerza la importancia de la **seguridad de identidad** dentro de la **arquitectura de datos en la nube**, asegurando que:

- Solo los usuarios adecuados accedan a los recursos correctos.  
- Las políticas estén alineadas con los entornos de **desarrollo, prueba y producción**.  
- Se mantenga la trazabilidad y cumplimiento normativo (GDPR, ISO 27001, etc.).  

La gestión de IAM forma parte esencial de toda **estrategia de Data Governance y Cloud Architecture**.

---

## 🧠 Reflexión Personal

> “Este proyecto me permitió comprender cómo la seguridad y la gobernanza de accesos son parte fundamental del diseño de arquitecturas cloud.  
> Crear políticas bien definidas es tan importante como diseñar la infraestructura misma.”

---

## 👨‍💻 Autor

**Angel G. Valdivia H.**  
Data & Cloud Specialist  
📧 agvaldivia86@gmail.com  

---

## 🪪 Licencia

Este proyecto fue desarrollado con fines **educativos** como parte del programa  
**NextWork – Cloud Security with AWS IAM**.
