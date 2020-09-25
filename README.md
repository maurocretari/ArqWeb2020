# AdminCar

Este sitio permite a los usuarios de autos registrar sus datos y los de sus vehiculos para luego recibir alertas sobre vencimientos de servicios, mantenimiento, etc.

Permite el Alta, Baja y Modificación de vehículos via API como así también la obtención de los vehículos pertenecientes a usuario

# ObtenerVehiculo

Método HTTP: GET
URL: /cars
Resultado: Entrega la lista de vehículos a la que el usuario que ejecuta la consulta tiene acceso.


Método HTTP: GET
URL: /cars/{id}
Resultado: Entrega la información del vehículo con ID = id


Método HTTP: GET
URL: /cars
QueryString: plate,year,color. Permite pasar las variables patente, año y color para filtrar la búsqueda.
Resultado: Entrega la información de los vehículos que coincidan con la búsqueda


# CrearVehiculo

Método HTTP: POST
URL: /cars
Params: plate, year, color
Resultado: Entrega la información del vehículo recien creado.
