# Proyecto-ia-Titanic

Cada vez que hagas cambios en cualquier archivo (README.md, Proyecto.py, etc.):
# 1. Guardar los cambios:
Presiona Ctrl + S o usa el menú para guardar los archivos modificados.

# 2. Verificar el estado de Git
En la terminal (PowerShell o integrada en Visual Studio), ejecuta:
git status
Esto te mostrará qué archivos están modificados o sin seguimiento.

# 3. Agregar los archivos que quieres subir (esto es para agregar otro archivo que fue necesario crear)
Para agregar un archivo específico:
git add nombre_del_archivo

O para agregar todos los cambios:
git add -A

# 4. Hacer un commit con un mensaje descriptivo
Ejecuta:
git commit -m "Mensaje que describa los cambios realizados"
Ejemplo: "Agrego función para preprocesar datos en Proyecto.py"

# 5. Subir los cambios al repositorio remoto en GitHub
Ejecuta:
git push origin main