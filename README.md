# AdminCar

Este sitio permite a los usuarios de autos registrar sus datos y los de sus vehiculos para luego recibir alertas sobre vencimientos de servicios, mantenimiento, etc.

Permite el Alta, Baja y Modificación de vehículos via API como así también la obtención de los vehículos pertenecientes a usuario

# ObtenerVehiculo

Método HTTP: GET\
URL: /cars\
QueryString (opcional): userid 
Resultado: Si no se especifica el userid entrega la lista de vehículos a la que el usuario que ejecuta la consulta tiene acceso, caso contrario entrega la lista del usuario con ID = userid\
Código HTTP Respuesta: 200


Método HTTP: GET\
URL: /cars/{id}\
Resultado: Entrega la información del vehículo con ID = id\
Código HTTP Respuesta: 200 (Si existe el vehículo), 404 (si no existe).


Método HTTP: GET\
URL: /cars\
QueryString: plate,year,color. Permite pasar las variables patente, año y color para filtrar la búsqueda.\
Resultado: Entrega la información de los vehículos que coincidan con la búsqueda\
Código HTTP Respuesta: 200 (Si existe el vehículo), 404 (si no existe).


# CrearVehiculo

Método HTTP: POST\
URL: /cars\
Params: plate, year, color\
Resultado: Entrega la información del vehículo recien creado.\
Código HTTP Respuesta: 201


# ModificarVehiculo

Método HTTP: PUT\
URL: /cars/{id}\
Params: plate, year, color\
Resultado: Entrega la información del vehículo con ID = id recién actualizado.\
Código HTTP Respuesta: 202
