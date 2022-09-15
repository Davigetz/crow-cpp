# crow-cpp

## Introduccion
Este proyecto se realizo con la intencion de ver la capacidad que utiliza c++ en parte web.

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
