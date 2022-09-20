# crow-cpp

## Introduccion
Este proyecto se realizo con la intencion de ver la capacidad que utiliza c++ en parte web y como ha cambiado su derrollo a travez del tiempo. Asi como mirar que tan facil o dificil es. 

## Objetivos
- Escribir una App con C++, Crow, Cmake, MongoDB, Javascript, HTML.
## Base de Datos
- MongoDB
## Instrucciones para Iniciar:
- Importante instalacion de drivers: mongo c, mongo c++ (3.6) o ultima version estable

### Archivo CMakeLists.txt tiene que:
```
CMAKE_PREFIX_PATH "/usr/local/mongo-cxx-driver/lib/cmake/libmongocxx-3.6.7" "/usr/local/mongo-cxx-driver/lib/cmake/libbsoncxx-3.6.7"
```
Tienes que reemplazar CMAKE_PREFIX_PATH con las rutas en donde encuentre los drivers de libmongocxx y libbsoncxx.<br>
```
include_directories(/usr/local/mongo-cxx-driver/include/mongocxx)
```
Tienes que reemplazar include_directories con las ruta en donde encuentre mongocxx.<br>

## Seguido
Tiene que inicializar la base de datos de mongodb

## <em>Con make en el computador y cmake intalados</em>
inicialize dentro de la carpeta build los siguientes comandos:
```
cmake ..
make
sudo bash ./compile.sh
```
- se realizaron una API asi como request y response desde el backend con mongodb.

## Images e Demo
![Screenshot from 2022-09-15 10-34-11](https://user-images.githubusercontent.com/19938780/190447868-f5eb5d73-4735-46a7-a4db-1fba3569b42b.png)

## Demostracion de websocket
[Screencast from 15-09-22 10:37:40.webm](https://user-images.githubusercontent.com/19938780/190448016-406d82b5-ebbd-48a8-878c-c0f0c66417a1.webm)

## Sacado del curso:
[Web Servers and APIs using C++](https://www.linkedin.com/learning/web-servers-and-apis-using-c-plus-plus/why-use-c-plus-plus-to-make-a-website?autoplay=true&resume=false)
## agradecimiento a:
[Troy Miles](https://www.linkedin.com/in/troy-miles-7516321/?trk=lil_instructor)
