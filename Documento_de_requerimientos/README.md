# Documento de Requerimientos

## Tabla de contenidos
- [Requerimientos Funcionales](#requerimientos-funcionales)
    - [Integración con brokers de pago](#Integración-con-brokers-de-pago)
    - [Integración con AFIP](#Integración-con-AFIP)
    - [Integración con los sistemas de empresa compradora](#Integración-con-los-sistemas-de-empresa-compradora)
    - [Manejo de stock digital](#Manejo-de-stock-digital)
    - [Informe diario de producción, compras y ventas](#Informe-diario-de-producción,-compras-y-ventas)
- [Requerimientos no Funcionales](#requerimientos-no-funcionales)
    - [Utilizar SUSE linux (Deseable)](#Utilizar-SUSE-linux-(Deseable))
    - [Operar en multiples plataformas digitales](#Operar-en-multiples-plataformas-digitales)
    - [Soportar 20.000 transacciones por hora](#Soportar-20.000-transacciones-por-hora)
    - [Manejar el stock digital a través del web site propio o un portal de venta](#Manejar-el-stock-digital-a-través-del-web-site-propio-o-un-portal-de-venta)
    - [Utilizar stack tecnológico con amplia comunidad de uso](#Utilizar-stack-tecnológico-con-amplia-comunidad-de-uso)
    - [Asegurar un RTO máximo de 1hs](#Asegurar-un-RTO-máximo-de-1hs)
- [Restricciones](#restricciones)
    - [Restricción 1](#Restricción-1)


## Requerimientos Funcionales
A continuación se listan los requerimientos funcionales del sistema:

- Integración con brokers de pago
- Integración con AFIP
- Integración con los sistemas de empresa compradora
- Manejo de stock digital
- Realizar informe diario

### Integración con brokers de pago
Esta integración consta de habilitar múltiples medios de pago, no solamente ventas online; aumentando el alcance de nuestra PyME.

### Integración con AFIP
Dicha integración tendrá la finalidad de realizar múltiples operaciones, como mínimo la facturación electrónica.

### Integración con los sistemas de empresa compradora
Una finalidad de este requerimiento es proveer a nuestra empresa compradora el informe diario producido, como por ejemplo, un informe de producción, compras y/o ventas. 

### Manejo de stock digital
Se busca realizar ventas las 24 horas del día, provocando la necesidad del manejo de stock de la producción. Si no se tuviera este manejo, se generarían inconsistencias y situaciones que provocan una experiencia negativa ante nuestros consumidores.

### Realizar informe diario
Este requerimiento surge por la necesidad de permitirle a la empresa compradora la funcionalidad de realizar auditorías, siendo completamente transparentes con la misma, ganandonos su fidelidad y atrayendo nuevas empresas.

## Requerimientos No Funcionales

A continuación se listan los requerimientos no funcionales del sistema:
- Utilizar SUSE linux (Deseable)
- Operar en multiples plataformas digitales
- Soportar 20.000 transacciones por hora
- Manejar el stock digital a través del web site propio o un portal de venta
- Utilizar stack tecnológico con amplia comunidad de uso
- Asegurar un RTO máximo de 1hs

### Utilizar SUSE linux *(Deseable)*
Se mantendrá como sistema operativo SUSE Linux, ya que cualquier solución es soportada en cualquier versión de Linux. 

### Operar en multiples plataformas digitales
Se garantizará al cliente accesibilidad, obteniendo desde cualquier dispositivo la misma experiencia.

### Soportar 20.000 transacciones por hora
Se espera un pico de 10.000 ventas por hora, conllevando la necesidad de manejar un promedio de 20.000 transacción por hora en total para que el sistema no colapse.

### Manejar el stock digital a través del web site propio o un portal de venta
Se garantizará manejo online de stock por cualquiera de los canales digitales, ya sea el website propio o portales de venta. 

### Utilizar stack tecnológico con amplia comunidad de uso
Se utilizará un stack tecnológico que cuente con una amplia comunidad que lo utilice, tanto desarrolladores como consumidores finales. 

### Asegurar un RTO máximo de 1hs
El sistema deberá garantizar un tiempo objetivo de recuperación de máximo 1 hora ante una posible caída del mismo.

## Restricciones:
Detalle de las Restricciones impuestas sobre el proyecto pero que no son restricciones sobre el producto, ejemplos son proceso de software a seguir, fechas de entrega, hitos de entrega fijos, etc

- Restricción 1

### Restricción 1
<Explicación>
