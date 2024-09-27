EJ5) 

EE1) COMIENZO
ACEPTAR DATOS_INTERNACION

SI DATOS_INTERNACION.NRO_ID = VACIO() ENTONCES 

CREAR ANIMALES CON 
CALCULAR ULT COMO ULTIMO NRO_ID EN ANIMALES
    nro_id = ult + 1
    nombre_animal = DATOS_INTERNACION.nro_animal
    especie = datos_internacion.especie
    raza = datos_internacion.raza
    sexo = datos_internacion.sexo
    fecha_nac = datos_internacion.fecha_nac
    dni = datos_internacion.dni
    apellido_res = datos_internacion.apellido_res
    nombre_resp = datos_internacion.nombre_resp
    domicilio = datos_internacion.domicilio
    tel = datos_internacion.tel
    estado_animal = "activo"
FIN CREAR 

CREAR INTERNACIONES CON 
CALCULAR ULT COMO ULTIMO nro_id EN INTERNACIONES 
    nro_id = ult + 1
    fecha_internacion = datos_internacion.fecha_internacion
    diagnostico = datos_internacion.diagnostico
    estado_internacion = "activa"
FIN CREAR

DE OTRO MODO 

CREAR INTERNACIONES CON 
    nro_id = datos_internacion.nro_id
    fecha_internacion = datos_internacion.fecha_internacion
    diagnostico = datos_internacion.diagnostico
    estado_internacion = "activa"
FIN CREAR

FIN SI 
FIN

EE2) COMIENZO
ACEPTAR DATOS_INTERVENCION 
    PARA CADA INTERVENCION EN INTERVENCIONES HACER        
        CREAR INTERVENCIONES CON 
        nro_id = datos_intervencion.nro_id
        fecha_internacion = datos_internacion.fecha_internacion
        fh_intervencion = INTERVENCION.fh_intervencion
        tipo_intervencion = intervencion.tipo_intervencion
        evolucion = intervencion.evolucion
        descripcion = intervencion.descripcion
        FIN CREAR
    FIN PARA CADA
FIN

EE3)
COMIENZO
    ACEPTAR DATOS_ALTA
    ACTUALIzar iNTERNACIONES CON FECHA_ALTA = HOY() Y ESTADO_INTERNACION = "CERRADA" DONDE NRO_ID = DATOS_ALTA.NRO_ID Y F"














































































