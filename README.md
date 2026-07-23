## 🚀 Cómo ejecutar el proyecto

### 1. Clonar el repositorio

```bash
git clone https://github.com/No-Country-simulation/g9-latam-techmind-team37.git
```

```bash
cd g9-latam-techmind-team37/data-science
```

### 2. Crear entorno virtual e instalar dependencias

```bash
py -m venv venv # venv\Scripts\activate
```

```bash
pip install -r requirements.txt
```

### 3. Levantar PostgreSQL con Docker

```bash
docker-compose up -d # PostgreSQL disponible en localhost:5432
```

### 4. Configurar variables de entorno y migrar datos

```bash
cd ..
```

```bash
cp .env.example .env
```

```bash
py data-science/src/migrate_to_postgres.py
```

### 5. Iniciar la API FastAPI

```bash
uvicorn app.main:app --reload --port 8000
```
