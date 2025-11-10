# Modelado-de-base-de-datos---Gesti-n-de-eventos-universitarios
# 🎓 Proyecto: Gestión de Eventos en una Universidad

##  Descripción

Este proyecto forma parte de la **Evaluación Sustitutoria – Unidad II** del curso **Modelado de Base de Datos**.  
El objetivo es diseñar e implementar una base de datos relacional que permita **gestionar los eventos universitarios**, registrando departamentos, ponentes, estudiantes y su participación.

---

##  Modelo Conceptual

El modelo conceptual representa las entidades y relaciones principales involucradas en la gestión de eventos.

**Entidades:**
- DEPARTAMENTO
- EVENTO
- ESTUDIANTE
- PONENTE
- PARTICIPACIÓN

**Relaciones:**
- Un **departamento** organiza varios **eventos** (1:N)  
- Un **evento** puede tener varios **ponentes** y viceversa (N:M)  
- Un **evento** puede tener varios **estudiantes** participantes y viceversa (N:M)  
  - Esta relación se resuelve mediante la entidad intermedia **Participación**

 Diagrama E-R disponible en:  
[`modelo_conceptual.png`](modelo_conceptual.png)

---

##  Modelo Lógico

**Tablas principales y claves:**
- **DEPARTAMENTO**(`id_departamento`, nombre, facultad)  
- **EVENTO**(`id_evento`, nombre, fecha_inicio, fecha_fin, lugar, id_departamento`)  
- **PONENTE**(`id_ponente`, nombre, especialidad, institucion`)  
- **ESTUDIANTE**(`id_estudiante`, nombre, carrera, correo`)  
- **PARTICIPACION**(`id_evento`, `id_estudiante`, asistencia, calificacion`)  
- **EVENTO_PONENTE**(`id_evento`, `id_ponente`)

---

## ⚙️ Modelo Físico (SQL)

El archivo `modelo_fisico.sql` contiene todas las sentencias `CREATE TABLE` necesarias para implementar la base de datos, incluyendo las **claves primarias** y **foráneas** que aseguran la integridad referencial.

 Archivo SQL:  
[`modelo_fisico.sql`](modelo_fisico.sql)

---

## 🧾 Informe en PDF

El documento principal del proyecto incluye:
- Modelo conceptual (E-R)
- Modelo lógico y físico
- Normalización y conclusiones

📘 Descargar informe:  
[`informe_modelado.pdf`](informe_modelado.pdf)

---

## 📂 Estructura del repositorio

