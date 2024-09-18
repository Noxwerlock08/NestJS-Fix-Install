# NestJS-Fix-Install

## Table of Contents

- [Descripción](#descripción)
- [Características](#características)
- [Requisitos](#requisitos)
- [Instalación](#instalación)
- [Uso](#uso)
- [Detalles del Script](#detalles-del-script)
- [Contribución](#contribución)
- [Licencia](#licencia)
- [Contacto](#contacto)

## Descripción

**NestJS-Fix-Install** es un script de PowerShell diseñado para solucionar problemas comunes al instalar el CLI de Nest.js en sistemas Windows. Este script automatiza la limpieza de la caché de `npm`, reinstala el CLI de Nest.js, y asegura que las rutas necesarias estén correctamente configuradas en las variables de entorno del sistema. Está especialmente útil para desarrolladores que enfrentan dificultades al configurar su entorno de desarrollo con Nest.js.

## Características

- **Limpieza de Caché de npm**: Elimina la caché de `npm` para prevenir conflictos y errores de instalación.
- **Reinstalación Automática del CLI de Nest.js**: Instala o reinstala el CLI de Nest.js globalmente.
- **Configuración de Variables de Entorno**: Verifica y agrega automáticamente la ruta global de `npm` al `PATH` del sistema.
- **Verificación de Instalación**: Confirma que el CLI de Nest.js esté correctamente instalado y accesible.
- **Interfaz Informativa**: Proporciona mensajes claros sobre el estado del proceso y cualquier acción requerida.

## Requisitos

- **Sistema Operativo**: Windows 10 o superior.
- **Permisos**: Privilegios de administrador para ejecutar el script.
- **Software Previo**:
  - [Node.js](https://nodejs.org/) (Incluye npm)

## Instalación

1. **Clonar el Repositorio**

    Abre PowerShell y ejecuta el siguiente comando para clonar el repositorio:

    ```powershell
    git clone https://github.com/Noxwerlock08/NestJS-Fix-Install.git

2. **Navegar al Directorio del Proyecto**

    ```powershell
     cd NestJS-Fix-Install
   
3. **Configurar la Política de Ejecución de PowerShell**

    Para permitir la ejecución de scripts, establece la política de ejecución a RemoteSigned para el usuario actual:

    ```powershell
     Set-ExecutionPolicy RemoteSigned -Scope CurrentUser
    ```
    > Nota: Si encuentras restricciones, asegúrate de ejecutar PowerShell como Administrador.

## Uso

1. **Abrir PowerShell como Administrador**

  Haz clic derecho en el ícono de PowerShell y selecciona "Ejecutar como administrador".

2. **Ejecutar el Script**

  Dentro del directorio del proyecto, ejecuta el script:

  ```powershell
  ./Fix-Nestjs.ps1
  ```
    
3. **Seguir las Instrucciones**

  El script realizará las siguientes acciones automáticamente:

- **Verificará si Node.js está instalado.**
- **Limpiará la caché de npm.**
- **Reinstalará el CLI de Nest.js globalmente.**
- **Verificará y actualizará las variables de entorno si es necesario.**
- **Confirmará que el CLI de Nest.js está funcionando correctamente.**
  
4. **Reiniciar la Terminal o el Sistema**

  Después de la ejecución, cierra y vuelve a abrir PowerShell o reinicia tu computadora para asegurarte de que los cambios en las variables de entorno se apliquen correctamente.

## Detalles del Script
El script Fix-Nestjs.ps1 realiza las siguientes operaciones paso a paso:

Verificación de Permisos de Administrador

Asegura que el script se ejecute con privilegios de administrador, necesarios para modificar variables de entorno del sistema.

Comprobación de la Instalación de Node.js

Verifica si Node.js está instalado y accesible en el sistema. Si no está instalado, solicita al usuario que lo instale.

Limpieza de la Caché de npm

Utiliza npm cache clean --force para eliminar la caché de npm, previniendo posibles conflictos o corrupciones.

Reinstalación del CLI de Nest.js

Instala el CLI de Nest.js globalmente mediante npm install -g @nestjs/cli.

Verificación de la Instalación del CLI de Nest.js

Comprueba si el CLI de Nest.js está correctamente instalado listando los paquetes globales y buscando @nestjs/cli.

Configuración de Variables de Entorno

Obtiene la ruta global de instalación de npm usando npm root -g.
Agrega la ruta de npm al PATH del sistema si no está presente, asegurando que los comandos globales como nest sean reconocidos.
Verificación Final del CLI de Nest.js

Ejecuta nest --version para confirmar que el CLI está instalado y accesible.

Notificación de Estado Final

Informa al usuario sobre el estado final del proceso y sugiere reiniciar el sistema si los cambios no se reflejan inmediatamente.

Contribución
¡Las contribuciones son bienvenidas! Si deseas mejorar este proyecto, sigue estos pasos:

Fork el repositorio.
Crea una rama para tu característica (git checkout -b feature/nueva-caracteristica).
Commit tus cambios (git commit -m 'Añadir nueva característica').
Push a la rama (git push origin feature/nueva-caracteristica).
Abre un Pull Request.
Por favor, asegúrate de seguir las guías de contribución si existen.

Licencia
Este proyecto está licenciado bajo la MIT License.

Contacto
Si tienes alguna pregunta o necesitas soporte, puedes contactarme a través de:

GitHub: Noxwerlock08
Correo Electrónico: noxwerlock08@example.com
¡Gracias por usar NestJS-Fix-Install! 🚀
