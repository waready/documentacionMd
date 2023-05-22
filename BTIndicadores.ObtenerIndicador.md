## Obtener Indicadores

Método para obtener los Indicadores por Agrupador

| Nombre publicación             | Programa | Global/País |
| ------------------------------ | -------- | ----------- |
| BTIndicadores.ObtenerIndicador | RBTPG702 | Global      |

> Ejemplo de invocación al servicio de Obtener Información Adicional:

```xml
<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/" xmlns:bts="http://uy.com.dlya.bantotal/BTSOA/">
   <soapenv:Header/>
   <soapenv:Body>
      <bts:BTIndicadores.ObtenerIndicador>
         <bts:Btinreq>
            <bts:Device>1</bts:Device>
            <bts:Canal>BTDIGITAL</bts:Canal>
            <bts:Token>959C2E0AEF210ABC0D8AA8F7</bts:Token>
            <bts:Usuario>INSTALADOR</bts:Usuario>
            <bts:Requerimiento>?</bts:Requerimiento>
         </bts:Btinreq>
         <bts:agrupadorId>100</bts:agrupadorId>
      </bts:BTIndicadores.ObtenerIndicador>
   </soapenv:Body>
</soapenv:Envelope>
```

```json
curl -X POST \
	'http://btd-bantotal.eastus2.cloudapp.azure.com:4462/btdeveloper/servlet/com.dlya.bantotal.odwsbt_BTClientes?ObtenerInformacionAdicional' \
	-H 'cache-control: no-cache' \
	-H 'content-type: application/json' \
	-H 'postman-token: 52baf1dc-e302-90a6-0de1-24fa234c0379' \
	-d '{
   "Btinreq": {
      "Device": 1,
      "Canal": "BTDIGITAL",
      "Token": "959C2E0AEF210ABC0D8AA8F7",
      "Usuario": "INSTALADOR",
      "Requerimiento": "?"
   },
   "agrupadorId": 100
}'
```

> El POST retornará la siguiente estructura:

```xml
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:SOAP-ENC="http://schemas.xmlsoap.org/soap/encoding/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
   <SOAP-ENV:Body>
      <BTIndicadores.ObtenerIndicadorResponse xmlns="http://uy.com.dlya.bantotal/BTSOA/">
         <Btinreq>
            <Device>1</Device>
            <Usuario>INSTALADOR</Usuario>
            <Requerimiento>?</Requerimiento>
            <Canal>BTDIGITAL</Canal>
            <Token>959C2E0AEF210ABC0D8AA8F7</Token>
         </Btinreq>
         <sdtIndicadores>
            <SdtsBTIndicador>
               <descripcion>Condiciones generales</descripcion>
               <codigo>105</codigo>
            </SdtsBTIndicador>
            <SdtsBTIndicador>
               <descripcion>Información de Cotizaciones</descripcion>
               <codigo>106</codigo>
            </SdtsBTIndicador>
         </sdtIndicadores>
         <Erroresnegocio></Erroresnegocio>
         <Btoutreq>
            <Numero>11989</Numero>
            <Estado>OK</Estado>
            <Servicio>BTIndicadores.ObtenerIndicador</Servicio>
            <Requerimiento>?</Requerimiento>
            <Fecha>2023-05-22</Fecha>
            <Canal>BTDIGITAL</Canal>
            <Hora>14:45:13</Hora>
         </Btoutreq>
      </BTIndicadores.ObtenerIndicadorResponse>
   </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
```

```json
{
   "Btinreq": {
      "Device": 1,
      "Usuario": "INSTALADOR",
      "Requerimiento": "?",
      "Canal": "BTDIGITAL",
      "Token": "959C2E0AEF210ABC0D8AA8F7"
   },
   "sdtIndicadores": {
      "SdtsBTIndicador": [
      {
         "descripcion": "Condiciones generales",
         "codigo": 105
      },
      {
         "descripcion": "Información de Cotizaciones",
         "codigo": 106
      }
      ]
   },
   "Erroresnegocio": "",
   "Btoutreq": {
      "Numero": 11989,
      "Estado": "OK",
      "Servicio": "BTIndicadores.ObtenerIndicador",
      "Requerimiento": "?",
      "Fecha": "2023-05-22",
      "Canal": "BTDIGITAL",
      "Hora": "14:45:13"
   }
}'
```

### Datos de entrada

| Nombre      | Tipo | Comentarios                 |
| ----------- | ---- | --------------------------- |
| agrupadorId | Int  | Identificador de Agrupador. |

### Datos de salida

| Nombre         | Tipo            | Comentarios                     |
| -------------- | --------------- | ------------------------------- |
| sdtIndicadores | SdtsBTIndicador | Informacion Adicional de datos. |

Los campos del tipo de dato estructurado SdtsBTIndicador son los siguientes:

| Campo       | Tipo   | Comentarios                 |
| ----------- | ------ | --------------------------- |
| codigo      | Int    | Identificador de Indicador. |
| descripcion | String | Descripción del Indicador.  |

### Errores

| Código | Descripción             |
| ------ | ----------------------- |
| 1      | No existen Indicadores. |
