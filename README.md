# GitHub Advanced Search - Instalador Windows

Este proyecto contiene el archivo HTML de GitHub Advanced Search y un script de Inno Setup para crear un instalador de Windows.

## Archivos del Proyecto

- **index.html** - Aplicación web de búsqueda avanzada en GitHub (sin modificaciones)
- **setup.iss** - Script de Inno Setup para crear el instalador de Windows

## Requisitos Previos

Para compilar el instalador necesitas:

1. **Inno Setup Compiler** - Descárgalo desde: https://jrsoftware.org/isdl.php
   - Versión recomendada: Inno Setup 6.x o superior
   - Instala la versión Unicode para mejor compatibilidad

## Cómo Compilar el Instalador

### Método 1: Usando Inno Setup Compiler (GUI)

1. Abre **Inno Setup Compiler**
2. Ve a `File` > `Open` y selecciona el archivo `setup.iss`
3. Presiona `F9` o ve a `Build` > `Compile`
4. El instalador se generará en la carpeta `Output` con el nombre `GitHubAdvancedSearch-Setup.exe`

### Método 2: Usando línea de comandos

```cmd
cd "C:\Users\Resec\CascadeProjects\GitHubSearchApp"
"C:\Program Files (x86)\Inno Setup 6\ISCC.exe" setup.iss
```

## Instalación de la Aplicación

1. Ejecuta `GitHubAdvancedSearch-Setup.exe`
2. Sigue el asistente de instalación
3. La aplicación se instalará en `C:\Program Files\GitHub Advanced Search\`
4. Se crearán iconos en:
   - Menú Inicio > GitHub Advanced Search
   - Escritorio (si seleccionaste la opción durante la instalación)

## Uso de la Aplicación

- La aplicación se abrirá en tu navegador predeterminado
- Funciona exactamente como la versión web original
- El token de GitHub se guarda en localStorage del navegador

## Personalización del Script .iss

Puedes personalizar el archivo `setup.iss` para:

- **Cambiar el nombre de la aplicación**: Modifica `AppName` y `AppVersion`
- **Cambiar el directorio de instalación**: Modifica `DefaultDirName`
- **Agregar un icono personalizado**: Descomenta y configura `SetupIconFile`
- **Agregar más archivos**: Agrega más entradas en la sección `[Files]`

## Solución de Problemas

### Error de compilación
- Asegúrate de que Inno Setup esté instalado correctamente
- Verifica que el archivo `index.html` esté en la misma carpeta que `setup.iss`

### La aplicación no se abre
- Verifica que tengas un navegador web instalado
- El archivo HTML se abrirá con tu navegador predeterminado

## Notas

- El archivo HTML no ha sido modificado
- La aplicación requiere conexión a internet para funcionar (usa la API de GitHub)
- Los datos del token se guardan localmente en el navegador del usuario
