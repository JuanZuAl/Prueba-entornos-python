# Configuración del proyecto

Instrucciones básicas para preparar el entorno de desarrollo. El proyecto usa **Python 3** con las librerías `pandas`, `matplotlib` y `seaborn`.

## Requisitos previos

- Python 3.11 o superior instalado (`python --version`)
- `pip` disponible (`pip --version`)

## 1. Crear el entorno virtual

Desde la raíz del proyecto:

```bash
python -m venv venv
```

Esto crea una carpeta `venv/` con el entorno aislado.

## 2. Activar el entorno virtual

**Windows (PowerShell):**

```powershell
.\venv\Scripts\Activate.ps1
```

> Si PowerShell bloquea la ejecución de scripts, ejecuta antes:
> `Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned`

**Windows (CMD):**

```cmd
venv\Scripts\activate.bat
```

**macOS / Linux:**

```bash
source venv/bin/activate
```

Sabrás que está activo porque el prompt mostrará `(venv)` al inicio.

## 3. Instalar las dependencias

Con el entorno activado, instala todo desde `requirements.txt`:

```bash
pip install -r requirements.txt
```

El archivo `requirements.txt` contiene:

```
pandas
matplotlib
seaborn
```

Para verificar la instalación:

```bash
pip list
```

## Generar / actualizar `requirements.txt`

Si agregas nuevas librerías, actualiza el archivo con:

```bash
pip freeze > requirements.txt
```

## Desactivar el entorno

```bash
deactivate
```

## Notas

- No subas la carpeta `venv/` al repositorio: agrégala a `.gitignore`.