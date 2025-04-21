

# 🛒 Supermercado con Inventario - Backend

Este repositorio contiene el backend de un sistema de gestión de inventarios para un supermercado. Desarrollado con **FastAPI**, ofrece una API rápida, robusta y escalable para administrar productos y operaciones relacionadas con el inventario.

---

## 🌟 **Descripción**

El backend de **Supermercado con Inventario** está diseñado para facilitar la gestión de inventarios mediante una API RESTful. Proporciona endpoints para realizar acciones como:

- Crear, leer, actualizar y eliminar productos.
- Gestionar categorías de productos.
- Consultar el estado del inventario.
- Registrar ventas y generar reportes.

Este backend puede conectarse fácilmente con un frontend o clientes externos.

---

## ✨ **Características**

- **Framework moderno**: Desarrollado con **FastAPI**, optimizado para alto rendimiento.
- **Documentación automática**: Swagger UI y ReDoc generados automáticamente para explorar y probar la API.
- **Base de datos relacional**: Integración con **SQLAlchemy** y soporte para bases de datos como SQLite, PostgreSQL o MySQL.
- **Autenticación**: Soporte para autenticación basada en tokens (JWT).
- **Código modular**: Arquitectura limpia y fácil de mantener.
- **Validación robusta**: Manejo de datos con **Pydantic** para garantizar integridad y seguridad.

---

## 🚀 **Cómo Empezar**

Sigue los pasos a continuación para configurar y ejecutar el backend en tu máquina local:

### 1. **Clona este repositorio**
   ```bash
   git clone https://github.com/jeanpaul615/SuperMercado-con-Inventario-BACKEND.git
   ```

### 2. **Accede al directorio del proyecto**
   ```bash
   cd SuperMercado-con-Inventario-BACKEND
   ```

### 3. **Crea un entorno virtual**
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```

### 4. **Instala las dependencias**
   ```bash
   pip install -r requirements.txt
   ```

### 5. **Configura las variables de entorno**
Crea un archivo `.env` en la raíz del proyecto con las siguientes variables:
   ```
   DATABASE_URL=sqlite:///./supermercado.db  # Cambia a PostgreSQL o MySQL según sea necesario
   SECRET_KEY=tu_clave_secreta
   ACCESS_TOKEN_EXPIRE_MINUTES=30
   ```

### 6. **Inicializa la base de datos**
   ```bash
   python app/db_init.py
   ```

### 7. **Ejecuta el servidor**
   ```bash
   uvicorn app.main:app --reload
   ```

El servidor estará disponible en `http://127.0.0.1:8000`.

---

## 📋 **Documentación de la API**

FastAPI genera automáticamente una interfaz de documentación interactiva:

- **Swagger UI**: [http://127.0.0.1:8000/docs](http://127.0.0.1:8000/docs)
- **ReDoc**: [http://127.0.0.1:8000/redoc](http://127.0.0.1:8000/redoc)

---

## 📂 **Estructura del Proyecto**

```
SuperMercado-con-Inventario-BACKEND/
├── app/
│   ├── main.py            # Punto de entrada principal
│   ├── models.py          # Definición de modelos SQLAlchemy
│   ├── schemas.py         # Definición de esquemas Pydantic
│   ├── routes/            # Endpoints de la API
│   ├── db_init.py         # Inicialización de la base de datos
│   └── utils.py           # Funciones auxiliares
├── tests/                 # Pruebas automatizadas
├── .env                   # Variables de entorno
├── requirements.txt       # Dependencias del proyecto
└── README.md              # Documentación
```

---

## 🛠️ **Requisitos**

- **Python 3.9 o superior**
- **FastAPI** (incluido en `requirements.txt`)
- **Uvicorn** para ejecutar el servidor.
- Base de datos (SQLite, PostgreSQL o MySQL).

---

## 🧪 **Pruebas**

Ejecuta las pruebas automatizadas con `pytest`:

```bash
pytest
```

---

## 🤝 **Contribuciones**

¡Las contribuciones son bienvenidas! Si tienes ideas para mejorar este backend o encuentras errores, sigue estos pasos:

1. Realiza un fork del repositorio.
2. Crea una nueva rama para tus cambios:
   ```bash
   git checkout -b feature/nueva-funcionalidad
   ```
3. Realiza tus cambios y haz un commit:
   ```bash
   git commit -m "Agrega nueva funcionalidad"
   ```
4. Envía tus cambios:
   ```bash
   git push origin feature/nueva-funcionalidad
   ```
5. Abre un [pull request](https://github.com/jeanpaul615/SuperMercado-con-Inventario-BACKEND/pulls).
