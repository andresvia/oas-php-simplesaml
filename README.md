# oas-php-simplesaml

## simplesaml

Pruebas locales:

 - Bajar Drone cli http://docs.drone.io/cli-installation/
 - Bajar requisitos: `drone exec --commit-sha=SNAPSHOT --privileged=oasplugins/s2i` (va a fallar por falta de credenciales para docker push [es normal])
 - Construir imagen: `s2i build --use-config`
 - Ejecutar imagen: `docker run -it --rm -p 8080 oas-php-simplesaml`
 - Abrir navegador en: `http://127.0.0.1:RANDOM_PORT/simplesaml`

Documentación hooks de s2i:

 - https://docs.openshift.com/container-platform/3.6/creating_images/s2i.html

Publicar la imagen:

`git commit -m "mi cambio" ; git push`

TODO:

 - Crear servicio ECS
 - Actualizar servicio ECS existente con `git push` (cambio a pipeline [`drone.yml`])
