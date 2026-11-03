# Trabajos Prácticos BD — Valentini & Garcia

**Integrantes:**
- Tiziano Valentini
- Juan Martin Garcia

**Cátedra:** Base de Datos II — Tecnicatura Universitaria en Programación (UTN FRM)  
**Comisión:** 2PRO4 — Ciclo Lectivo 2026  
**Docente:** Sergio Neira  

Repositorio institucional `Trabajos-Practicos-BD-Valentini-Garcia` dedicado a las entregas integrales de Trabajos Prácticos de Base de Datos.

---

## Módulos y Entregables del Repositorio

### 1. [TP8_Movil_SQLite_Cierre — Unidad 8: La Base de la Tablet y Cierre de la Capa de Datos](TP8_Movil_SQLite_Cierre/README.md)
* **Temática:** Sincronización offline-first asimétrica ("El móvil propone, el servidor dispone"), base SQLite 3.37+ con tipado `STRICT` y claves foráneas activas, motor de resolución por semáforo de estados (`PENDIENTE`, `CONFLICTO`, `RECHAZADO`, `SIMULADO_APROBADO`), instantáneas con precios en centavos enteros y lápidas de soft-delete, mapa arquitectónico de 3 motores (PostgreSQL, MongoDB, SQLite), plan de contingencia y code review de la cursada con IA.
* **Archivos clave:**
  - `TP8_Movil_SQLite_Cierre/movil/schema_sqlite.sql`: DDL SQLite STRICT.
  - `TP8_Movil_SQLite_Cierre/movil/pruebas_sqlite.sql`: Transacciones, Caso C1 y Caso C7.
  - `TP8_Movil_SQLite_Cierre/movil/vista_postgres_snapshot.sql` y `servidor_snapshot.csv`: Instantánea central.
  - `TP8_Movil_SQLite_Cierre/movil/semaforo.sql`: Consulta SQL de resolución offline.
  - `TP8_Movil_SQLite_Cierre/movil/simulador.py`: Orquestador de simulación de Casos C2 a C6 y generador de `foodstore_movil.db`.
  - `TP8_Movil_SQLite_Cierre/docs/informe.md`: Informe técnico integrador completo.
  - `TP8_Movil_SQLite_Cierre/docs/kiro/`: Especificación formal EARS (`requirements.md`, `design.md`, `tasks.md`).
  - `TP8_Movil_SQLite_Cierre/docs/bitacora_ia.md` y `DUIA.md`: Registro de uso ético de IA con descartes técnicos fundados.

### 2. [TP8_NoSQL_MongoDB — Unidad 7: NoSQL y Nuevas Formas de Almacenamiento](TP8_NoSQL_MongoDB/README.md)
* **Temática:** Modelado documental desnormalizado en MongoDB (`pedidos`), migración JSONB desde PostgreSQL, consultas analíticas con Aggregation Pipeline y verificación cruzada contra consultas relacionales equivalentes con `JOIN`.
* **Archivos clave:**
  - `TP8_NoSQL_MongoDB/consultas_mongodb.js`: Scripts de creación y agregación en `mongosh`.
  - `TP8_NoSQL_MongoDB/consultas_postgresql.sql`: Consultas relacionales de verificación cruzada en PostgreSQL.
  - `TP8_NoSQL_MongoDB/informe_nosql_mongodb.md`: Informe técnico y benchmarking de motores.

---

## Guía Rápida de Ejecución

### Unidad 8 — Base Móvil y Sincronización SQLite (TP8)
```bash
# Ejecución automatizada de simulación y generación de base SQLite:
python TP8_Movil_SQLite_Cierre/movil/simulador.py

# Verificación de vista y datos en PostgreSQL:
psql -U postgres -d food_store_dev -f TP8_Movil_SQLite_Cierre/movil/vista_postgres_snapshot.sql
```

### Unidad 7 — Persistencia Documental MongoDB
```bash
# Ejecución en MongoDB shell:
mongosh TP8_NoSQL_MongoDB/consultas_mongodb.js

# Verificación relacional en PostgreSQL:
psql -U postgres -d food_store_dev -f TP8_NoSQL_MongoDB/consultas_postgresql.sql
```
