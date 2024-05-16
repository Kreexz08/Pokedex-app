# Despliegue en Azure

## Pasos utilizados para el despliegue

#### 1. Nos vamos a git y usamos los comandos npm install y npm run build con el proyecto
#### 2. Esto nos creara una carpeta llamada dist, la cual tiene el contenido que desplegaremos en el app service, tal como se puede ver a continuacion:
![evidencia](https://github.com/Kreexz08/Pokedex-app/assets/141959642/6ff91291-c0fd-42a6-aa34-d3d67be9e907)

#### 3. Ingresamos al portal azure 
#### 4. Creamos el grupo de recursos
#### 5. Creamos la app web como se muestra a continuacion:
![evidencia 1](https://github.com/Kreexz08/Pokedex-app/assets/141959642/ea62d8c4-b874-4fdb-9c12-b082531d5f42)

#### 6 Luego creamos y nos dirigimos al recurso
#### 7 Nos dirigimos a la seccion de herramientas de desarrollo y dentro de este a herramientas avanzadas:
![evidencia 2](https://github.com/Kreexz08/Pokedex-app/assets/141959642/dd4b0b1e-0e72-4074-8ed1-7124deac46e3)

#### 8. Presionamos en Debug console>CMD 
#### 9. Nos dirigimos en las carpetas site>wwwroot y en esta desplegamos, subiendo los archivos del dist en esta como se muestra a continuacion:
![evidencia 3](https://github.com/Kreexz08/Pokedex-app/assets/141959642/fd1bb07e-2e68-4864-8338-7fdbffd6c749)

#### Despues de esto funcionara la aplicacion como se ve a continuacion:
![evidencia 4](https://github.com/Kreexz08/Pokedex-app/assets/141959642/c33e1dcc-290f-4ee7-b54d-527dc841bba0)

#### Pero tendra problemas de seguridad en los encabezados de los headers y para esto lo configuraremos
#### 10. Creamos un archivo llamado web.config
#### 11. Le agregamos las directivas para seguridad y luego de esto miramos bien que no se haya afectado los estilos y revisamos en la pagina https://securityheaders.com/
#### en la pagina ponemos el enlace de la aplicacion, en este caso el de la mia es app-pokedex.azurewebsites.net y a continuacion se muestra los resultados:
![evidencia 5](https://github.com/Kreexz08/Pokedex-app/assets/141959642/c9914964-579b-4678-92eb-ba8d98b07091)

#### En este caso no salio A+ porque al quitar la directris "unsafe-inline" en los scripts se pierden algunos estilos en la vista porque usan Javascript, pero si se hace, saldra A+ como se puede ver a continuacion:
![evidencia 6](https://github.com/Kreexz08/Pokedex-app/assets/141959642/55319d49-daa4-459d-9d94-c253649722bd)


