<div align="center">
<picture>
    <source srcset="https://imgur.com/5bYAzsb.png" media="(prefers-color-scheme: dark)">
    <source srcset="https://imgur.com/Os03JoE.png" media="(prefers-color-scheme: light)">
    <img src="https://imgur.com/Os03JoE.png" alt="Escudo UNAL" width="350px">
</picture>

<h3>Curso de Robótica 2025-I</h3>

<h1>Introducción a Linux</h1>

<h2>Guía 00 - Instalación y Uso Básico de Ubuntu 22.04 LTS</h2>


<h5>Pedro Fabián Cárdenas Herrera<br>
    Manuel Felipe Carranza Montenegro</h5>

</div>

<div align="justify">
## Introducción

En el desarrollo de sistemas de robótica moderna, inteligencia artificial y automatización, contar con un entorno operativo estable, flexible y compatible con las principales herramientas de software es fundamental. Linux, con su variedad de distribuciones, se ha consolidado como el sistema operativo por excelencia en estos ámbitos.

Entre todas las distribuciones disponibles, **Ubuntu 22.04 LTS** ha sido adoptada como estándar por múltiples comunidades y plataformas, incluido **ROS 2 Humble Hawksbill**, debido a su equilibrio entre estabilidad a largo plazo y soporte actualizado de herramientas. Sin embargo, existen diferentes formas de instalar Ubuntu y diversas distribuciones que también pueden cumplir este rol, lo cual motiva un análisis comparativo.

Este documento busca guiar al usuario en la elección de la opción más adecuada según sus necesidades, ya sea que trabaje en desarrollo local, virtualizado, en entornos de contenedores o sistemas híbridos.

## Objetivos

- **Presentar las principales opciones de instalación de Ubuntu 22.04 LTS**, comparando su funcionalidad, ventajas y limitaciones según el entorno de trabajo.
- **Comparar Ubuntu 22.04 con otras distribuciones Linux relevantes**, evaluando criterios como estabilidad, soporte, facilidad de uso y compatibilidad con ROS 2.
- **Justificar la elección de Ubuntu 22.04 LTS** como entorno recomendado para proyectos educativos, académicos o industriales relacionados con robótica y desarrollo de software.
- **Brindar una herramienta clara y accesible** que facilite la toma de decisiones a estudiantes, investigadores o desarrolladores que desean configurar su entorno Linux de forma óptima.

## Comparativa de Distribuciones Linux para Desarrollo y Robótica

La elección de una distribución Linux adecuada es crucial para asegurar un entorno de desarrollo estable, seguro y compatible con las herramientas tecnológicas actuales. En áreas como la robótica, donde se requiere compatibilidad con ROS2, facilidad de mantenimiento y soporte comunitario, no todas las distribuciones ofrecen el mismo nivel de rendimiento.

A continuación, se presenta un análisis comparativo de las principales distribuciones Linux utilizadas en contextos de desarrollo y robótica. El objetivo es resaltar sus ventajas, limitaciones y su grado de compatibilidad con ROS2, para justificar la elección de Ubuntu 22.04 LTS como la alternativa más adecuada para estos entornos.


| Distribución           | Estabilidad | Compatibilidad con ROS2 | Soporte de la Comunidad | Facilidad de Uso | Ciclo de Soporte | ¿Por qué no se elige?                                                                 |
|------------------------|-------------|---------------------------|--------------------------|------------------|------------------|---------------------------------------------------------------------------------------|
| **Ubuntu 22.04 LTS**   | Alta      | Excelente (ROS2 Humble está diseñado para esta versión) | Enorme          | Alta           | 5 años LTS      | -                                                                                     |
| Debian                 | Muy alta  | Parcial (requiere ajustes para ROS2)                    | Grande           | Media          | Estable         | - Requiere instalación y configuración más manual.                                    |
| Fedora                 | Media     | Experimental/limitada                                    | Menor           | Moderna         |  Ciclo corto     | - Cambios frecuentes pueden romper compatibilidad con herramientas como ROS.         |
| Arch Linux             |  Inestable | No recomendado (paquetes muy recientes y sin soporte oficial) |  Comunidad técnica |  Avanzado        |  Rolling release | - Demasiado inestable para proyectos de largo plazo o académicos.                    |
| CentOS / Rocky Linux   |  Alta      |  No soportado oficialmente                                 |  Limitada         |  Media          |  Larga duración  | - Enfocado a servidores, no al desarrollo o robótica.                                |
| Pop!_OS                |  Alta      |  Compatible con ROS2                                      |  Activa           |  Muy amigable    |  Mediano         | - No es una LTS oficial soportada directamente por ROS2.                            |
| Linux Mint             |  Alta      |  Compatible con ROS2 (basado en Ubuntu)                  |  Amigable         |  Muy fácil       |  LTS             | - Enfoque más generalista, no optimizado para desarrollo técnico.                    |

---

## ¿Por qué se elige **Ubuntu 22.04 LTS**?

Ubuntu 22.04 LTS es la opción preferida porque:

- **ROS2 Humble Hawksbill** fue diseñado específicamente para esta versión.
- Tiene **compatibilidad total con herramientas de desarrollo** modernas como Docker, Python 3.10, OpenCV, TensorFlow, etc.
- Ofrece un **equilibrio ideal entre estabilidad y actualidad** de paquetes.
- Cuenta con una **amplia comunidad de soporte**, documentación oficial y foros activos.
- Es ampliamente utilizada en entornos académicos, laboratorios de investigación y la industria.

## Métodos de Instalación

Antes de comenzar a trabajar con Ubuntu 22.04 LTS y ROS2, es importante definir la forma en la que se instalará el sistema operativo. Existen distintos métodos para hacerlo, cada uno con ventajas y limitaciones según los recursos del equipo, el nivel de experiencia del usuario y los objetivos del proyecto.

En esta sección se comparan los métodos más comunes para ejecutar Ubuntu, desde instalaciones nativas hasta entornos virtualizados y contenedores. Esta comparativa busca ayudar al usuario a seleccionar la opción más adecuada según sus necesidades de rendimiento, compatibilidad y flexibilidad.

| Método de instalación          | Descripción                                                                     | Ventajas                                                                                                        | Desventajas                                                                                  |
|-------------------------------|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| **Instalación Nativa**        | Ubuntu reemplaza al sistema operativo actual.                                   | - Máximo rendimiento y estabilidad.  <br> - Acceso completo al hardware.  <br> - Sin problemas de compatibilidad.   | - Elimina otros sistemas si no se respalda.  <br> - Mayor tiempo de configuración inicial.         |
| **Dual Boot**                 | Ubuntu se instala en una partición junto a Windows.                             | - Máximo rendimiento.  <br> - Permite elegir entre Windows y Ubuntu al arrancar.  <br> - Acceso directo al hardware. | - Requiere particionar el disco.  <br> - No se pueden usar ambos sistemas al mismo tiempo.         |
| **Máquina Virtual (VM)**      | Ubuntu corre dentro de Windows usando VirtualBox, VMware, etc.                  | - Fácil de instalar/eliminar.  <br> - Ejecuta Ubuntu y Windows simultáneamente.                                     | - Rendimiento inferior.  <br> - Problemas con entornos gráficos pesados y ROS2.                    |
| **WSL2**                      | Ubuntu corre dentro de Windows sin máquina virtual.                             | - Instalación sencilla.  <br> - Intercambio de archivos con Windows.  <br> - Menor consumo que VM.                  | - Soporte limitado para ROS2 GUI/simuladores.  <br> - Acceso limitado a USB y GPU.                 |
| **Contenedores (Docker)**     | Ubuntu y ROS2 corren en un contenedor sin modificar el sistema anfitrión.      | - Aislamiento del sistema.  <br> - Portabilidad.  <br> - No modifica el SO principal.                               | - Configuración compleja.  <br> - Acceso limitado a GPU y sensores.   

## Instrucciones de Instalación según el Método

### Instalación Nativa

1. Descargar la ISO de Ubuntu 22.04 LTS desde la web oficial: [ubuntu.com](https://releases.ubuntu.com/jammy/).
2. Crear un USB booteable usando herramientas como **Rufus** (Windows) o **balenaEtcher** (Linux/macOS).
3. Reiniciar el equipo e ingresar al BIOS/UEFI (usualmente con `F2`, `F12`, `Del` o `Esc`) para seleccionar el USB como dispositivo de arranque.
4. Seleccionar “Instalar Ubuntu” y seguir las instrucciones del asistente.
5. Elegir “Borrar disco e instalar Ubuntu” para reemplazar el sistema actual.
6. Configurar nombre de usuario, contraseña y zona horaria.
7. Finalizar la instalación, retirar el USB y reiniciar el sistema.

> Este método elimina el sistema operativo anterior. Asegúrate de hacer copia de seguridad.

---

### Dual Boot (Ubuntu + Windows)

1. Crear una partición libre en tu disco duro desde Windows (mínimo 25 GB recomendados).
2. Descargar la ISO de Ubuntu 22.04 LTS.
3. Crear USB booteable con **Rufus** o **balenaEtcher**.
4. Reiniciar el equipo e iniciar desde el USB.
5. Seleccionar “Instalar Ubuntu” > “Instalar junto a Windows”.
6. Elegir cuánto espacio ocupará Ubuntu con el deslizador.
7. Continuar con la instalación y configuración.
8. Al reiniciar, aparecerá un menú (GRUB) para elegir entre Windows o Ubuntu.

---

### Máquina Virtual (VirtualBox/VMware)

1. Descargar Ubuntu 22.04 LTS ISO.
2. Instalar **VirtualBox** o **VMware Workstation Player**.
3. Crear una nueva máquina virtual:
   - Asignar mínimo 2 núcleos, 4 GB de RAM y 50 GB de disco.
4. Montar la ISO como disco de arranque.
5. Iniciar la máquina virtual y seguir el proceso de instalación estándar de Ubuntu.
6. Instalar **Guest Additions** (VirtualBox) para mejorar el rendimiento y soporte gráfico.

#### Intalación VMWare
https://github.com/user-attachments/assets/d33ad01a-0f71-42c8-a730-a9789a8949c6

#### Intalación Ubuntu 22.04 LTS - VMWare
https://github.com/user-attachments/assets/8e603200-b8d1-4dae-872e-257750d92b8a

#### Intalación Ubuntu 22.04 LTS - Virtual Box
https://github.com/user-attachments/assets/8d22f098-0147-427b-837d-ce8a527d1816

---

### WSL2 (Windows Subsystem for Linux)

1. Asegúrate de tener **Windows 10 versión 2004 o superior** o **Windows 11**.
2. Abre PowerShell como administrador y ejecuta:

   ```powershell
   wsl --install
   ```
3. Espera a que se instalen los componentes necesarios. Reinicia el sistema si se solicita.
4. Abre Microsoft Store y busca Ubuntu 22.04 LTS. Haz clic en "Obtener" para instalarlo.
5. Una vez instalado, ábrelo desde el menú de inicio. Se configurará por primera vez.
6. Crea un usuario y contraseña para tu sistema Ubuntu.
7. Ya puedes usar la terminal de Ubuntu dentro de Windows.
8. Para instalar ROS 2 Humble, sigue las instrucciones oficiales:
[ROS2 Humble en Ubuntu](https://docs.ros.org/en/humble/)

> Si necesitas interfaz gráfica (RViz, Gazebo, etc.), instala un servidor X como VcXsrv o considera otra opción.

#### Intalación WSL2
https://github.com/user-attachments/assets/f3c41b45-3433-4dae-81b3-c95dded44e12

---

### Contenedores (Docker)
1. Instala Docker Desktop desde: [Docker](docker.com/products/docker-desktop)
2. Asegúrate de activar el backend de WSL2 durante la instalación si estás en Windows.
3. Verifica que Docker esté funcionando abriendo una terminal y ejecutando:
    ```powershell
    docker --version
    ```
4. Descarga una imagen oficial de ROS 2 con Ubuntu (por ejemplo, ROS 2 Humble con entorno gráfico):
    ```powershell
    docker pull osrf/ros:humble-desktop
    ```
5. Crea y ejecuta un contenedor interactivo:
    ```powershell
    docker run -it osrf/ros:humble-desktop
    ```
6. (Opcional) Monta una carpeta local para guardar tu trabajo:
    ```powershell
    docker run -it -v /ruta/local:/home/ros_user/workspace osrf/ros:humble-desktop
    ```
7. Puedes instalar herramientas adicionales dentro del contenedor como si estuvieras en Ubuntu.

> Docker es ideal si quieres un entorno limpio, replicable, y no deseas modificar tu sistema actual.

## Principales Comandos de Ubuntu

| Comando                          | Función                                                                 |
|----------------------------------|-------------------------------------------------------------------------|
| `pwd`                            | Muestra la ruta del directorio actual.                                 |
| `ls`                             | Lista los archivos y carpetas del directorio actual.                   |
| `cd nombre_directorio`          | Cambia al directorio especificado.                                     |
| `cd ..`                          | Sube un nivel en la estructura de carpetas.                            |
| `cd ~`                           | Va al directorio personal del usuario (`/home/usuario`).               |
| `mkdir nombre`                  | Crea una nueva carpeta.                                                |
| `rm nombre`                     | Elimina un archivo.                                                    |
| `rm -r carpeta`                 | Elimina una carpeta y todo su contenido.                               |
| `cp origen destino`             | Copia un archivo o carpeta a otra ubicación.                           |
| `mv origen destino`             | Mueve o renombra un archivo o carpeta.                                 |
| `touch nombre_archivo`          | Crea un archivo vacío.                                                 |
| `nano archivo`                  | Abre un editor de texto en terminal (nano).                            |
| `cat archivo`                   | Muestra el contenido de un archivo.                                    |
| `sudo comando`                  | Ejecuta el comando como superusuario (administrador).                  |
| `apt update`                    | Actualiza la lista de paquetes disponibles.                            |
| `apt upgrade`                   | Instala las últimas versiones de los paquetes disponibles.             |
| `apt install nombre_paquete`   | Instala un programa o paquete.                                         |
| `apt remove nombre_paquete`    | Elimina un paquete instalado.                                          |
| `clear`                         | Limpia la terminal.                                                    |
| `history`                       | Muestra el historial de comandos utilizados.                           |
| `df -h`                         | Muestra el uso del espacio en disco en formato legible.                |
| `top`                           | Muestra los procesos en ejecución (como el administrador de tareas).   |
| `ps aux`                        | Lista todos los procesos activos.                                      |
| `kill PID`                      | Finaliza un proceso mediante su ID.                                    |
| `chmod`                         | Cambia los permisos de archivos o carpetas.                            |
| `chown`                         | Cambia el propietario de archivos o carpetas.                          |
| `ping direccion_ip`            | Verifica la conectividad de red con una dirección.                     |
| `ifconfig` / `ip a`            | Muestra información de red (IP, interfaces, etc.).                     |
| `tar -czvf archivo.tar.gz carpeta/` | Comprime una carpeta en formato tar.gz.                            |
| `tar -xzvf archivo.tar.gz`     | Descomprime un archivo tar.gz.                                         |
| `man comando`                  | Muestra el manual de ayuda de un comando.                              |
| `exit`                          | Sale de la terminal o sesión actual.                                   |
</div>

