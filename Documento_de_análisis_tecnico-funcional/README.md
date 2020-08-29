# Documento de análisis tecnico-funcional

## Tabla de contenidos
- [Documento de Análisis Técnico-Funcional](#documento-de-análisis-técnico-funcional)
    - [Transacciones](#Transacciones)
    - [Ventas del negocio](#Ventas-del-negocio)
    - [Integración con portales de venta](#Integración-con-portales-de-venta)
    - [Integración con AFIP](#Integración-con-AFIP)
    - [Manejo del stock](#Manejo-del-stock)
    - [Integración con brokers de pago](#Integración-con-brokers-de-pago)
    - [Integración con la empresa compradora](#Integración-con-la-empresa-compradora)
    - [Tiempo de recuperación objetivo](#Tiempo-de-recuperación-objetivo)
    - [Punto de recuperación objetivo](#Punto-de-recuperación-objetivo)

## Documento de Análisis Técnico-Funcional
Este documento tiene como objetivo determinar la brecha técnico-funcional existente entre la solución actual de la empresa y la solución que se espera alcanzar. Así mismo, se analiza punto por punto los cambios que hay que realizar, indicando la brecha correspondiente.

### Transacciones
**Situación Actual**: 3.600 transacciones por hora.  
**Situación Deseada**: 20.000 transacciones por hora.  
**Brecha**: se necesita aumentar en, por lo menos, 16.400 las transacciones por hora.  

### Ventas del negocio
**Situación Actual**: se realizan ventas en el local y a través de Mercado Libre.  
**Situación Deseada**: desarrollar un website de ventas propio multiplataforma.  
**Brecha**: se debe desarrollar una página web multiplataforma para realizar ventas propias (la misma deberá desarrollarse desde cero, ya que actualmente no se cuenta con un website propio).  

### Integración con portales de venta
**Situación Actual**: no existe integración con ningún portal de venta.  
**Situación Deseada**: integrar el sistema con los portales de venta más conocidos.  
**Brecha**: se debe desarrollar una página web multiplataforma para realizar ventas propias (la misma deberá desarrollarse desde cero, ya que actualmente no se cuenta con un website propio).  

### Integración con AFIP
**Situación Actual**: se emiten las facturas manualmente.  
**Situación Deseada**: integrar el sistema con los portales de venta más conocidos.  
**Brecha**: se deberá realizar la integración con AFIP para realizar las facturas automáticamente ante la venta de un producto. Hoy en día, esto se realiza de manera manual.    

### Manejo del stock
**Situación Actual**: se maneja el stock manualmente.  
**Situación Deseada**: manejo de stock online.  
**Brecha**: se deberá agregar a la base de datos, el stock actual de la empresa para así poder llevar un control automático a la hora de realizar las ventas. Además, se deberá crear un backoffice para poder dar de alta, baja y modificacion el stock en el sistema.  

### Integración con brokers de pago
**Situación Actual**: actualmente el sistema solo soporta los medios de pago que Mercado Libre brinda. Esta apreciación es únicamente para los medios de venta digitales.  
**Situación Deseada**: integrar el sistema actual con al menos dos brokers de pago.   
**Brecha**: se deberá integrar con los brokers de pago más conocidos del mercado, inicialmente con mercadopago y paypal, además de tarjetas de credito y debito para ventas online.   

### Integración con la empresa compradora
**Situación Actual**: el sistema no se encuentra integrado con los sistemas de la empresa compradora, dado que la compra se realizó recientemente.  
**Situación Deseada**: se integrará el sistema con los sistemas de la empresa compradora.  
**Brecha**: se le proveerá a la empresa compradora una API para la integración de la misma al sistema existente actualmente. Esta API contemplará el control de producción, de compras, de ventas y de stock.   

### Tiempo de recuperación objetivo
**Situación Actual**: el RTO actual no está medido.  
**Situación Deseada**: RTO máximo de 1 hs.  
**Brecha**: dado que la app es muy simple ya que cuenta con todos los controles manuales, y el servidor tiene muy buenas características, se presume que hoy en día cuenta con un RTO bajo. Con la solución se agregara un servidor nuevo en otro data center para evitar que ante problemas físicos del servidor haya una afectación al servicio.  

### Punto de recuperación objetivo
**Situación Actual**: el RPO actual no está medido.  
**Situación Deseada**: RPO igual a 0.  
**Brecha**: dado que los servidores cuentan con discos espejados, se forma un RAID 1, con lo cual en caso de un fallo, se puede levantar el otro disco evitando la pérdida de datos (salvo la información que podría haber entrado mientras el sistema estuvo caído). En caso de una falla en algún otro componente del servidor, va a implicar que estemos fuera de servicio, por lo que se va a implementar un balanceador de carga. En caso de algún daño físico al servidor, el balanceador va a distribuir todas las transacciones a los servidores que continúen operando.  