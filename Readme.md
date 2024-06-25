# Aplicación de Control de Gastos

Esta es una aplicación web para el control de gastos personales. Permite a los usuarios registrar sus ingresos y gastos, gestionar presupuestos y generar informes detallados sobre sus finanzas.

## Tecnologías Utilizadas

- **Backend:**
  - Django
  - Django REST Framework
  - PostgreSQL

- **Frontend:**
  - React
  - Axios

- **Contenedores:**
  - Docker
  - Docker Compose

## Requisitos Previos

- Docker y Docker Compose instalados en tu máquina.
- Node.js y npm instalados (para desarrollo frontend).

## Configuración Inicial

### Clonar el Repositorio

```bash
git clone https://github.com/bead-code/AppGastos.git
cd AppGastos
```

### Configuración del Backend

1. Crear y activar un entorno virtual (opcional pero recomendado):
```bash
cd backend
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
```

2. Instalar dependencias:
```bash
pip install -r requirements.txt
```

3. Configurar variables de entorno:
Crear un archivo `.env` en el directorio `backend/` y agregar las variables necesarias:
```env
DEBUG=True
SECRET_KEY=tu_clave_secreta
DATABASE_NAME=nombre_bd
DATABASE_USER=usuario_bd
DATABASE_PASSWORD=clave_bd
DATABASE_HOST=db
DATABASE_PORT=5432
```

4. Aplicar migraciones y crear un superusuario:
```bash
python manage.py migrate
python manage.py createsuperuser
```

## Configuración del Frontend
1. Instalar dependencias:

```bash
cd frontend
npm install
```
2. Configurar variables de entorno:

Crear un archivo `.env` en el directorio `frontend/` y agregar las variables necesarias:

```env
REACT_APP_API_URL=http://localhost:8000/api/
```

# Ejecución del Proyecto

## Usando Docker Compose

1. Ejecutar Docker Compose:
```bash
docker-compose up --build
```
2. Acceder a la aplicación:
- Backend: http://localhost:8000/admin/
- Frontend: http://localhost:3000/

## Ejecución Manual (Desarrollo)

### Backend

1. Ejecutar el servidor de desarrollo de Django:
```bash 
cd backend
python manage.py runserver
```

### Frontend
```bash
cd frontend
npm start
```

# Notas Adicionales
- Asegúrate de tener PostgreSQL corriendo si no estás usando Docker.
- Configura correctamente las variables de entorno tanto para desarrollo como para producción.
- Consulta la documentación de Django y React para más detalles sobre el desarrollo y configuración de la aplicación.

# Contribuciones
Las contribuciones son bienvenidas. Por favor, abre un issue para proponer ideas o envía un pull request para discutir cualquier cambio.