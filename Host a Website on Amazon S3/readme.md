# 🌐 Host a Website on Amazon S3

![AWS](https://img.shields.io/badge/AWS-S3-orange?logo=amazonaws)
![Status](https://img.shields.io/badge/Status-Completed-success)
![License](https://img.shields.io/badge/License-Educational-blue)
![Made with ❤️](https://img.shields.io/badge/Made%20with-%E2%9D%A4-red)

---

## 🧠 Descripción del Proyecto

Este proyecto demuestra cómo **alojar un sitio web estático en Amazon S3**, aplicando conceptos fundamentales de AWS y buenas prácticas de permisos y accesos.

> 💬 “Mi objetivo fue aprender los fundamentos de AWS de forma práctica, entendiendo cómo se configuran buckets, permisos y endpoints públicos.”

---

## 🧰 Tecnologías y Conceptos Utilizados

| Servicio / Concepto | Descripción |
|----------------------|-------------|
| **Amazon S3** | Servicio de almacenamiento de objetos para alojar archivos del sitio web. |
| **ACLs (Access Control Lists)** | Configuración de permisos a nivel de objeto y bucket. |
| **Static Website Hosting** | Funcionalidad de S3 para servir sitios web estáticos públicamente. |
| **Bucket Endpoint** | URL pública generada por S3 para acceder al sitio. |
| **403 Forbidden Resolution** | Solución de errores de acceso mediante permisos públicos. |

---

## 🗂️ Pasos del Proyecto

### 1️⃣ Crear el Bucket S3
- Se creó un bucket en la región **South America (São Paulo) – `sa-east-1`**.  
- La región fue elegida por su **baja latencia** y **cumplimiento de residencia de datos**.  
- Los nombres de buckets deben ser **únicos globalmente**, ya que forman parte del dominio del endpoint.

---

### 2️⃣ Subir Archivos del Sitio
- Archivos utilizados:
  - `index.html` — estructura principal del sitio.  
  - `images.zip` — recursos visuales del sitio.  

---

### 3️⃣ Habilitar Static Website Hosting
1. Activar “**Static website hosting**”.  
2. Seleccionar “**Host a static website**”.  
3. Definir **`index.html`** como documento de inicio.  

---

### 4️⃣ Configurar Permisos y ACLs
- Inicialmente apareció un error **403 Forbidden**.  
- La causa fue la falta de permisos públicos.  
- Se resolvió configurando los objetos como **públicos** mediante **ACLs**.

---



---

## ✅ Resultado Final

El sitio web fue **publicado exitosamente** y es accesible públicamente.  
El proceso permitió comprender cómo AWS gestiona **permisos, hosting y distribución de contenido**.

---

## 📸 Vista Previa del Sitio

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/1/1b/Amazon_S3_logo.svg" width="120" alt="AWS S3 Logo" />
</p>

> *(Reemplaza esta imagen con una captura real de tu sitio cuando esté en línea, por ejemplo: `/assets/preview.png`)*

---

## 💡 Reflexión Personal

> “El mayor aprendizaje fue entender cómo resolver errores de acceso y manejar ACLs correctamente.  
> Ver el sitio activo fue la mejor recompensa de este proyecto práctico.”

---

## 🔗 Enlaces Útiles

- 🌍 [NextWork Community](https://community.nextwork.org)  
- 💬 [Discusión del Proyecto](https://community.nextwork.org/c/i-have-a-question?automatic_login=true)

---

## 👨‍💻 Autor

**Ángel G. Valdivia H.**  
NextWork Student | Data & Cloud Enthusiast  
📧 agvaldivia86@gmail.com

---

## 🪪 Licencia

Este proyecto fue desarrollado con fines **educativos** como parte del programa **NextWork Student Projects**.
