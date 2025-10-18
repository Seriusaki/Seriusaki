# 🛡️ Seguridad en la Nube con AWS IAM

**Autor:** Ángel G. Valdivia H.  
**Rol:** Data & Cloud Specialist  
**Plataforma:** NextWork  
**Proyecto:** Cloud Security with AWS IAM  
**Duración aproximada:** ~1 hora  
**Herramientas:** AWS IAM, EC2, Políticas JSON, Tags  

---

## 🧭 Descripción del Proyecto

En este proyecto demuestro cómo **AWS Identity and Access Management (IAM)** permite gestionar el acceso a instancias **EC2** mediante **grupos de usuarios** y **políticas personalizadas**.  
El objetivo fue aplicar el **principio de privilegio mínimo**, diseñar un modelo de permisos seguro y separar los accesos entre los entornos de **desarrollo** y **producción**.

---

## ⚙️ Herramientas y Conceptos

- **AWS IAM** → gestión de usuarios, grupos y políticas.  
- **EC2** → entorno de prueba para validación de permisos.  
- **Políticas JSON** → para definir reglas de acceso precisas.  
- **Etiquetas (Tags)** → utilizadas para controlar accesos por entorno (`development` / `production`).  
- **Account Alias** → configuración de una URL personalizada para el inicio de sesión.  
- **Onboarding seguro** → distribución de credenciales mediante CSV o correo cifrado.

---

## 🧱 Relación con la Arquitectura de Datos

Dentro de una arquitectura moderna de datos, la **seguridad y gobernanza de acceso** son fundamentales.  
La implementación de IAM permite:

- Definir **roles y permisos** segmentados por entorno (desarrollo, pruebas, producción).  
- Controlar el acceso a **datasets sensibles** y servicios de datos en la nube.  
- Integrar la seguridad de identidad con servicios como **S3, Glue o Redshift**.  
- Cumplir con normativas de **gobernanza y compliance** (por ejemplo, GDPR o ISO 27001).

---

## 🏷️ Etiquetas (Tags)

Utilicé etiquetas para diferenciar entornos y aplicar políticas basadas en contexto.  
Las etiquetas usadas fueron:

- `development`  
- `production`  

Esto permitió restringir operaciones en producción y habilitarlas solo en recursos de desarrollo.

---

## 🧩 Política IAM

Se creó una **política personalizada en formato JSON**, con el objetivo de controlar las acciones sobre EC2.  
La política fue diseñada para:

- Permitir únicamente acciones en instancias etiquetadas como `development`.  
- Dar acceso de solo lectura a todos los recursos EC2.  
- Bloquear la creación o eliminación de etiquetas.  

Esta configuración garantizó un **acceso controlado, seguro y con privilegio mínimo** para los usuarios internos.

---

## 👥 Usuarios y Grupos IAM

- **Usuarios:** identidades individuales con credenciales propias.  
- **Grupos:** conjuntos de usuarios con permisos compartidos.

En este caso, la política se asignó a un **grupo de internos**, de modo que todos los usuarios del grupo heredan los mismos permisos y limitaciones.

---

## 🔐 Métodos de Acceso y Validación

Los usuarios IAM recibieron sus credenciales mediante dos métodos posibles:

1. Envío directo por correo electrónico.  
2. Archivo `.csv` generado en AWS con las claves de acceso.

Durante las pruebas:

- Al intentar detener la instancia de **producción**, el sistema mostró “Access Denied”.  
- Al intentar detener la instancia de **desarrollo**, la acción fue **exitosa**.  

Esto confirmó que la política funcionaba correctamente y aplicaba el **principio de privilegio mínimo**.

---

## 🌐 Alias de Cuenta

Para mejorar la facilidad de uso, se configuró un **alias de cuenta** que reemplaza el ID numérico por un nombre legible.  
Esto permite ingresar a la consola mediante una URL


---

## 💡 Lecciones Aprendidas

- Las políticas JSON requieren **precisión y validación constante**.  
- Las **etiquetas (tags)** son esenciales para separar entornos y mantener control operativo.  
- La **seguridad de identidad** es un componente clave dentro de la **arquitectura de datos en la nube**.  
- Implementar el **principio de privilegio mínimo** fortalece la gobernanza y la confianza en los sistemas.

---

## 🧠 Reflexión Personal

> “Diseñar políticas IAM reforzó mi enfoque en la seguridad y gobernanza como partes esenciales de la arquitectura de datos.  
> Un entorno bien estructurado y con permisos controlados no solo protege los datos, sino que mejora la eficiencia y escalabilidad del ecosistema cloud.”

---

📍 **Proyecto desarrollado como parte del programa “Cloud Security with AWS IAM – NextWork”**

