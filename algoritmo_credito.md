INICIO
    LEER ingresos_mensuales, deudas_mensuales, puntaje_crediticio, monto_solicitado, años_de_empleo

    relacion_deuda_ingreso = deudas_mensuales / ingresos_mensuales
    cuota_estimada = monto_solicitado / 36

    SI puntaje_crediticio < 600 ENTONCES
        MOSTRAR "Crédito rechazado: puntaje insuficiente"
    SINO SI relacion_deuda_ingreso > 0.40 ENTONCES
        MOSTRAR "Crédito rechazado: endeudamiento alto"
    SINO SI cuota_estimada > ingresos_mensuales * 0.30 ENTONCES
        MOSTRAR "Crédito rechazado: la cuota supera el 30% de los ingresos"
    SINO SI años_de_empleo < 1 ENTONCES
        MOSTRAR "Enviar a revisión manual"
    SINO
        MOSTRAR "Crédito aprobado"
    FIN SI
FIN
