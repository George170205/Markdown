# Guía Rápida de Instalación de Python

## Indice
- [Introduccion](#encabezados)

- [Consideraciones Previas](#consideraciones-previas)

- [Instalacion en Windows](#instalación-en-windows)

- [Instalación en macOS](#instalación-en-macos)

- [Instalación en Linux](#instalación-en-linux)

- [Instalacion de paquetes](#instalación-de-paquetes)

- [Errores y dudas frecuentes](#errores-y-dudas-frecuentes)





## Introducción

Python es un lenguaje de programación versátil utilizado en desarrollo, ciencia de datos, inteligencia artificial, aprendizaje automático, _scripting_ y automatización. Su diseño enfatiza la legibilidad del código con una sintaxis limpia y espacios en blanco significativos, siendo ideal tanto para principiantes como para programadores experimentados.

## Consideraciones Previas

Antes de instalar Python, es importante considerar que existen dos ramas principales: Python 2.x (obsoleta desde enero 2020) y Python 3.x (versión actual recomendada). Para la instalación necesitarás conocimientos básicos de informática, familiaridad con la línea de comandos y una conexión a Internet. Los requisitos mínimos incluyen 4GB de RAM y 5GB de espacio libre en disco.

## Instalación en Windows

### Método 1: Desde el Sitio Web Oficial

1. **Descarga el instalador**
   
   Visita el sitio web oficial de Python y descarga el instalador adecuado para tu sistema (32 o 64 bits).

   Ve a [python.org](https://www.python.org/downloads/)

   <img src=img2.jpg width=600>

2. **Ejecuta el instalador**
   
   Haz doble clic en el archivo descargado. Es posible que necesites dar permiso al Control de Cuentas de Usuario.

   <img src=img5.jpg width=500>

3. **Configura la instalación**
   
   IMPORTANTE: Marca la casilla "Add Python 3.x to PATH" antes de continuar. Puedes elegir "Instalar ahora" para una configuración predeterminada o "Personalizar instalación" para más opciones.

4. **Completa la instalación**
   
   Haz clic en Instalar para iniciar el proceso. Al finalizar, verás un mensaje de éxito.


5. **Verifica la instalación**
   
   Abre el Símbolo del sistema (CMD) o PowerShell y escribe `python --version`. Deberías ver la versión instalada.

   <img src=img3.jpg width=500>

---

### Método 2: Microsoft Store

Este método es altamente recomendado para usuarios principiantes, ya que simplifica el proceso sin necesidad de configurar variables de entorno manualmente.

**Pasos:**
1. Abre la **Microsoft Store**.
2. Busca **"Python"**.
3. Selecciona la versión más reciente de Python (por ejemplo, *Python 3.x*).
4. Haz clic en **Instalar**.

**Verificación (en PowerShell o CMD):**
```bash
python --version
```
O si no reconoce `python`:

```bash
python3 --version
```

---

### Método 3: Anaconda

Anaconda incluye Python junto con muchas librerías para ciencia de datos y análisis numérico, como NumPy, Pandas y Jupyter.

**Pasos:**
1. Ve a [https://www.anaconda.com/products/distribution](https://www.anaconda.com/products/distribution).
2. Descarga el instalador para Windows.
3. Ejecuta el instalador y sigue las instrucciones del asistente.

**Verificación (en PowerShell o CMD):**
```bash
conda --version
```

---

## Instalación en macOS

macOS incluye una versión de Python, pero generalmente es una versión antigua usada por el sistema. Es recomendable instalar una versión más reciente.

**Verificación de la versión preinstalada:**
```bash
python3 --version
```

---

### Método 1: Sitio Web Oficial

**Pasos:**
1. Visita [https://www.python.org/downloads/macos/](https://www.python.org/downloads/macos/).
2. Descarga el instalador más reciente compatible con macOS.
3. Ejecuta el archivo `.pkg` descargado y sigue los pasos.

**Verificación en Terminal:**
```bash
python3 --version
```

---

### Método 2: Homebrew

Homebrew es un gestor de paquetes útil para instalar software en macOS.

**Pasos:**
1. Si no tienes Homebrew, instálalo con el siguiente comando en Terminal:
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

2. Una vez instalado, ejecuta:
```bash
brew install python3
```

**Verificación:**
```bash
python3 --version
```

---

### Método 3: Anaconda

**Pasos:**
1. Visita [https://www.anaconda.com/products/distribution](https://www.anaconda.com/products/distribution).
2. Identifica si tu Mac tiene procesador Intel o Apple Silicon (M1/M2).
3. Descarga el instalador correspondiente.
4. Sigue los pasos del asistente gráfico.

**Verificación:**
```bash
conda --version
```

---

## Instalación en Linux

La mayoría de las distribuciones de Linux ya incluyen Python preinstalado.

**Verificación:**
```bash
python3 --version
```

---

### Método 1: Gestor de Paquetes

Usa el gestor de paquetes de tu distribución para instalar o actualizar Python.

- **Ubuntu / Debian:**
```bash
sudo apt update
sudo apt install python3
```

- **Fedora:**
```bash
sudo dnf install python3
```

**Verificación:**
```bash
python3 --version
```

---

### Método 2: Compilación desde Código Fuente

Este método está destinado a usuarios avanzados que requieren una versión personalizada de Python.

**Pasos generales:**
```bash
sudo apt update
sudo apt install -y build-essential libssl-dev zlib1g-dev \
  libncurses5-dev libncursesw5-dev libreadline-dev libsqlite3-dev \
  libgdbm-dev libdb5.3-dev libbz2-dev libexpat1-dev liblzma-dev tk-dev

wget https://www.python.org/ftp/python/3.x.y/Python-3.x.y.tgz
tar -xvf Python-3.x.y.tgz
cd Python-3.x.y
./configure --enable-optimizations
make -j$(nproc)
sudo make altinstall
```

**Verificación:**
```bash
python3.x --version
```
_Reemplaza `3.x` con la versión que hayas instalado._

## Instalación de Paquetes

Una vez instalado Python, puedes extender su funcionalidad con paquetes adicionales:

- Si instalaste Python desde el sitio oficial o Microsoft Store, usa `pip3` para gestionar paquetes:
  - Instalar: `pip3 install nombre_paquete`
  - Actualizar: `pip3 install --upgrade nombre_paquete`
  - Desinstalar: `pip3 uninstall nombre_paquete`
  - Listar paquetes: `pip3 freeze`

- Si instalaste Python a través de Anaconda, usa `conda`:
  - Instalar: `conda install nombre_paquete`
  - Actualizar: `conda update nombre_paquete`
  - Desinstalar: `conda remove nombre_paquete`
  - Listar paquetes: `conda list`


## Errores y dudas frecuentes

### Windows

#### Errores comunes
- **"Python no está reconocido como un comando interno o externo, programa o archivo por lotes ejecutable"**: 
  - **Causa**: Python no está agregado al PATH del sistema.
  - **Solución**: 
    1. Reinstala Python y marca la casilla "Add Python to PATH" durante la instalación.
    2. O añade manualmente Python al PATH:
       - Busca "Variables de entorno" en el menú inicio
       - En Variables del sistema, selecciona "Path" y haz clic en "Editar"
       - Añade la ruta completa a Python (ej. `C:\Python310` y `C:\Python310\Scripts`)
       - Reinicia el símbolo del sistema o PowerShell

- **"Se produjo un error al intentar ejecutar el instalador"**:
  - **Causa**: Permisos insuficientes o archivos dañados.
  - **Solución**: 
    1. Ejecuta el instalador como administrador (clic derecho → Ejecutar como administrador)
    2. Descarga nuevamente el instalador desde python.org

- **Conflictos entre versiones de Python**:
  - **Causa**: Múltiples instalaciones de Python en el sistema.
  - **Solución**: 
    1. Usa el comando `py` con la versión específica: `py -3.10` o `py -3.11`
    2. Especifica la ruta completa del ejecutable: `C:\Python310\python.exe`
    3. Usa Python Launcher para gestionar múltiples versiones

- **Error al instalar paquetes con pip**:
  - **Causa**: Problemas con permisos o configuración de pip.
  - **Solución**:
    1. Ejecuta el símbolo del sistema como administrador
    2. Usa `python -m pip install nombrePaquete` en lugar de solo `pip install`
    3. Actualiza pip con `python -m pip install --upgrade pip`

#### Dudas frecuentes

- **¿Debo instalar Python 32 o 64 bits?**
  - En sistemas modernos, casi siempre deberías optar por la versión de 64 bits, que ofrece mejor rendimiento y manejo de memoria.

- **¿Cómo puedo verificar si Python está correctamente instalado?**
  - Abre el símbolo del sistema y escribe `python --version` o `py --version`.

- **¿Cómo instalo Python sin interfaz gráfica?**
  - Descarga el instalador y ejecutalo desde la línea de comandos con: `python-3.x.x.exe /quiet InstallAllUsers=1 PrependPath=1`

- **¿Es necesario desinstalar versiones anteriores?**
  - No es obligatorio, pero es recomendable para evitar conflictos, especialmente si no necesitas mantener proyectos en versiones antiguas.

### macOS

#### Errores comunes

- **"Command not found: python"**:
  - **Causa**: macOS Catalina y posterior ya no incluyen Python 2 preinstalado.
  - **Solución**: 
    1. Usa `python3` en lugar de `python`
    2. Crea un alias en tu archivo `.zshrc` o `.bash_profile`: `alias python=python3`

- **"Permission denied" al instalar paquetes**:
  - **Causa**: Permisos insuficientes para escribir en directorios del sistema.
  - **Solución**: 
    1. Usa `pip install --user nombrePaquete` para instalar solo para tu usuario
    2. Utiliza entornos virtuales con `venv` o `conda`
    3. Como último recurso, usa `sudo pip3 install nombrePaquete` (no recomendado)

- **Problemas con SSL durante la instalación de paquetes**:
  - **Causa**: Certificados SSL desactualizados o problemas con la configuración.
  - **Solución**:
    1. Actualiza los certificados con: `pip install --upgrade certifi`
    2. En casos extremos: `pip install --trusted-host pypi.org --trusted-host files.pythonhosted.org nombrePaquete`

- **Conflictos con la versión preinstalada de Python**:
  - **Causa**: macOS viene con Python para uso del sistema.
  - **Solución**:
    1. No modifiques la versión del sistema, instala otra versión para tu uso
    2. Usa Homebrew: `brew install python`
    3. Usa pyenv para gestionar múltiples versiones: `pyenv install 3.10.0`

#### Dudas frecuentes

- **¿Debo usar la versión de Python que viene con macOS?**
  - No es recomendable. Es mejor instalar tu propia versión para desarrollo.

- **¿Cómo instalo Python en macOS?**
  - Opciones: Instalador oficial desde python.org, Homebrew (`brew install python`), o pyenv.

- **¿Homebrew vs Instalador oficial?**
  - Homebrew facilita las actualizaciones y la gestión de paquetes, pero el instalador oficial es más directo.

- **¿Cómo ejecuto scripts Python con doble clic?**
  - Añade `#!/usr/bin/env python3` al inicio del script y dale permisos de ejecución con `chmod +x script.py`.

### Linux

#### Errores comunes

- **"ModuleNotFoundError" al importar módulos instalados**:
  - **Causa**: Instalación en la versión incorrecta de Python.
  - **Solución**:
    1. Verifica qué versión estás usando: `python --version` vs `python3 --version`
    2. Instala el paquete específicamente para tu versión: `python3 -m pip install nombrePaquete`

- **Conflictos entre pip y el gestor de paquetes del sistema**:
  - **Causa**: Instalación dual de paquetes Python.
  - **Solución**:
    1. Usa entornos virtuales para proyectos
    2. Prioriza el gestor de paquetes del sistema para paquetes globales
    3. No uses `sudo pip` para evitar sobrescribir paquetes del sistema

### Anaconda

#### Errores comunes

- **Conflictos de entorno con Anaconda**:
  - **Causa**: Activación incorrecta de entornos o rutas conflictivas.
  - **Solución**:
    1. Asegúrate de inicializar conda correctamente: `conda init bash` (o tu shell)
    2. Usa `conda activate nombreEntorno` para activar entornos específicos
    3. Verifica el entorno activo con `conda info --envs`

- **"PackagesNotFoundError" al instalar paquetes**:
  - **Causa**: El paquete no está disponible en los canales configurados.
  - **Solución**:
    1. Añade canales adicionales: `conda install -c conda-forge nombrePaquete`
    2. Si no está disponible en conda, usa pip como alternativa dentro del entorno conda





