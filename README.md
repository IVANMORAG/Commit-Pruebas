# Git Activity Simulator

## Descripción
Un script en Bash diseñado para generar commits aleatorios en un repositorio Git, simulando actividad de desarrollo. Permite configurar un rango de fechas y establece diferentes cantidades de commits según el día de la semana (más actividad en días laborales, menos en fines de semana). Ideal para pruebas, demostraciones o para poblar un repositorio con historial de commits.

## Características

* **Rango de fechas configurable:** Define un período para generar commits.
* **Commits variables por día:**
  
  * Lunes a viernes: 5-15 commits.
    
  * Sábados y domingos: 1-5 commits.

* **Horarios aleatorios:** Cada commit se realiza en una hora, minuto y segundo aleatorios dentro del día.
* **Commits vacíos:** No requiere cambios reales en los archivos, usa --allow-empty.
* **Automatización completa:** Genera y sube los commits al repositorio remoto.

## Requisitos

* Entorno Linux/Unix con Bash.
  
* Git instalado y configurado.
* Acceso de escritura al repositorio Git y permisos para hacer push al remoto.

## Uso

* Clona el repositorio:
  ```bash
  git clone <URL_DEL_REPOSITORIO>
  ```

* Navega al directorio del proyecto:
  ```bash
  cd git-activity-simulator
  ```

* Asegúrate de que el script tiene permisos de ejecución:
  ```bash
  chmod +x script.sh
  ```

* Edita las variables ***start_date*** y ***end_date*** en el script para definir el rango de fechas deseado.

* Ejecuta el script:
  ```bash
  ./script.sh
  ```

* Los commits se generarán y se subirán automáticamente al branch **main**.

## Ejemplo

Para simular actividad desde el 12 de enero de 2025 hasta el 20 de marzo de 2025, configura:
```bash
start_date="2025-01-12"
end_date="2025-03-20"
```
El script generará commits aleatorios en ese período y los subirá al repositorio remoto.

## Estructura del Proyecto

* **script.sh:** Script principal que genera los commits.

## Contribuir

¡Las contribuciones son bienvenidas! Si deseas mejorar el script, por favor:

* Haz un fork del repositorio.
  
* Crea una nueva rama (git checkout -b feature/nueva-funcionalidad).
* Realiza tus cambios y haz commit (git commit -m 'Añadir nueva funcionalidad').
* Sube tu rama (git push origin feature/nueva-funcionalidad).
* Crea un Pull Request.

## Licencia
Este proyecto está bajo la Licencia MIT. Consulta el archivo LICENSE para más detalles.

## Aviso

**Este script es para fines educativos o de prueba. Úsalo de manera responsable y evita generar actividad excesiva en repositorios de producción.**
