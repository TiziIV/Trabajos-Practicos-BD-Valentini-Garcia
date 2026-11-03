# Trabajos Prácticos BD — Valentini & Garcia

**Integrantes:**
- Tiziano Valentini
- Juan Martin Garcia

Repositorio institucional `Trabajos-Practicos-BD-Valentini-Garcia` dedicado a las entregas de Trabajos Prácticos de Base de Datos. Actualmente contiene la **Unidad 7: NoSQL y Nuevas Formas de Almacenamiento (MongoDB)**.

---

## Estructura del Entregable

Todo el desarrollo, scripts ejecutables, informe técnico y evidencia cruzada se encuentran organizados en la carpeta [`TP8_NoSQL_MongoDB`](TP8_NoSQL_MongoDB/README.md):

1. **`TP8_NoSQL_MongoDB/consultas_mongodb.js`**: Script íntegro y ejecutable en `mongosh`. Crea la base `food_store_nosql`, colección `pedidos`, migra los documentos embebidos mediante `insertMany()` y ejecuta las 4 consultas analíticas solicitadas en la Consigna 4.
2. **`TP8_NoSQL_MongoDB/consultas_postgresql.sql`**: Script en PostgreSQL con la consulta de extracción / serialización JSONB de pedidos y las consultas relacionales equivalentes con `JOIN` para validación cruzada.
3. **`TP8_NoSQL_MongoDB/informe_nosql_mongodb.md`**: Informe técnico exhaustivo (listo para exportar a PDF) que aborda las 6 consignas del TP: modelado documental vs relacional, justificación de embedding, evidencias de ejecución, tabla de verificación cruzada, contraste de respuestas de IA contra documentación oficial y conclusiones arquitectónicas.
4. **`TP8_NoSQL_MongoDB/README.md`**: Guía técnica detallada con los requisitos previos y las instrucciones paso a paso para la reproducción local de los scripts.

---

## Instrucciones Rápidas de Ejecución

### 1. MongoDB (`mongosh`)
```bash
# Conexión local estándar
mongosh TP8_NoSQL_MongoDB/consultas_mongodb.js

# O mediante npx (sin instalación global previa)
npx mongosh TP8_NoSQL_MongoDB/consultas_mongodb.js
```

### 2. PostgreSQL (`psql`)
```bash
# Conexión psql a la base de datos de desarrollo
psql -U postgres -d food_store_dev -f TP8_NoSQL_MongoDB/consultas_postgresql.sql
```
